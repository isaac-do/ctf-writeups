---
date: 2026-05-11
tags:
  - cyberdefenders
  - cloud-forensics
  - jq
  - cloudwatch
  - cloudtrail
---
# Lab Overview
---
**Lab:** [AWSWatcher Lab](https://cyberdefenders.org/blueteam-ctf-challenges/awswatcher/)  
**Platform:** CyberDefenders  
**Category:** Cloud Forensics  
**Difficulty:** Easy  
**Tools:** CloudWatch, CloudTrail, jq  

# Summary
---
This lab investigates a web application attack against an AWS-hosted platform where an attacker exploited an XML data processing endpoint vulnerable to XXE injection. Using the vulnerability, the attacker accessed internal AWS metadata and resources, leading to unauthorized access to misconfigured S3 buckets and exfiltration of sensitive records before the security team could respond.

# Scenario
---
Between 20 and 25 February 2025, Compliant Secure Store recently launched its new website, but security misconfigurations left critical gaps. Soon after the launch, an attacker initiated widespread scanning and discovered an upload feature that processed XML data without proper validation. By crafting a specially designed payload, the attacker manipulated the system’s input handling, triggering unintended data exposure.

Using the extracted information from this vulnerability, the attacker authenticated into the system and navigated internal resources. During the exploration, misconfigured storage buckets were discovered, and sensitive records were exfiltrated before the security team could intervene.

Your mission is to analyze the attack flow, identify exploited weaknesses, and implement the necessary security controls to prevent future incidents.

# Analysis
---
## During the initial scanning, the attacker interacted with the web application from an external IP address. What is the origin IP tied to the attacker, as observed in the AWS logs?

To begin this investigation, in CloudWatch Log Insights, we'll first set the date to Feb 20 through Feb 25 2025.  
![](../../../../attachments/attachment-awswatcher-lab-05122026-1.png)  

Lambda function logs "Received events" which contains the JSON structure of the API Gateway event. We'll query for `received event` logs then perform a REGEX search for source IP addresses in the JSON structure.  
```sql
fields @timestamp, @message 
| filter @message like /Received event/ 
| parse @message /sourceIp["\s:]+(?<clientIP>\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})/ 
| stats count() as cnt by clientIP 
| sort cnt desc
```
- The `(?<clientIP>\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})` is a named capture group that extracts IPv4 addresses and store it in a field called `clientIP`  

The query resulted in two IP addresses: `41.46.53.241` and `154.178.195.103`. Based on its high appearance count, the IP address actively interacting with the file upload functionality and making suspicious requests is `41.46.53.243`.  
![](../../../../attachments/attachment-awswatcher-lab-05122026.png)  

## A code review uncovered a function that lacked proper input validation, enabling arbitrary file processing. Which function’s misconfiguration directly enabled the initial exploit?

Lambda function logs are stored in log groups that follow the format `/aws/lambda/[FunctionName]`. To verify this, we can run the query below to check the function name that appears in execution records.  
```sql
fields @timestamp, @message
| filter @message like /REPORT/ or @message like /START/ or @message like /END/
| limit 10
```
![](../../../../attachments/attachment-awswatcher-lab-05122026-2.png)  

Based on the current log group `/aws/lambda/FileUpload` and the result from the query, the function that is misconfigured and vulnerable is `FileUpload`.  

## The attacker uploaded a file masquerading as a benign document but containing an embedded malicious payload. What’s the filename of the `SVG` payload disguised as a financial record?

We can broadly search through the lambda logs for message that contains either `.SVG` or `SVG` and `financial`.  
```sql
fields @timestamp, @message
| filter (@message like /.svg/ or @message like /svg/) and @message like /financial/
| sort @timestamp asc
```

The query returned an event at 2025-02-25 09:55:41 where a file named `financial_statement_2143.svg` was uploaded.  
![](../../../../attachments/attachment-awswatcher-lab-05122026-4.png)  

## During analysis of the CloudWatch Logs, the attacker’s external IP address was observed invoking an API to upload files to an S3 bucket. What is the **exact URL path** used for this upload operation, as seen in the logs?

We'll search for events that contain the word `upload` to find upload-specific paths and also include the attacker's IP address.  
```sql
fields @timestamp, @message
| filter @message like /upload/ and @message like /41\.46\.53\.241/
| limit 5
```

In the screenshot below, we can observe the full file path for file uploads is `/prod/dev/upload`. Based on this name, there is likely a misconfiguration since both `prod` and `dev` appear in the same path.  
![](../../../../attachments/attachment-awswatcher-lab-05122026-6.png)  

To obtain the full URL path, we'll combine the full path `/prod/dev/upload` with the API Gateway domain name `upilqcjrp5.execute-api.us-east-1.amazonaws.com` to get `https://upilqcjrp5.execute-api.us-east-1.amazonaws.com/prod/dev/upload`.  

## Which IAM role with excessive permissions was abused during the attack and used to query sensitive S3 buckets?

Navigate to `aws-cloudtrail-logs-149536493376-f6e00302/AWSLogs/149536493376/CloudTrail/us-east-1/2025/02/23/` and download the log file `149536493376_CloudTrail_us-east-1_20250223T0055Z_d0om30WedJHjcc8O.json.gz` and extract it.  

Using jq, run the command below to search the vulnerable function `FileUpload` and output the user identity.  
```bash
jq '.Records[] | select(.userIdentity.principalId | test("FileUpload")) | {eventTime: .eventTime, userIdentity: .userIdentity}' 149536493376_CloudTrail_us-east-1_20250223T0055Z_d0om30WedJHjcc8O.json
```

The abused IAM role is `LambdaParser`.  
![](../../../../attachments/attachment-awswatcher-lab-05122026-7.png)  

## What is the MITRE ATT&CK technique related to the attacker’s use of valid cloud credentials to log into the system?

MITRE technique `T1078.004` allows adversaries to perform actions to achieve Initial Access, Persistence, Privilege Escalation, or Defense Evasion.  
![](../../../../attachments/attachment-awswatcher-lab-05122026-8.png)  

## A server error inadvertently disclosed a temporary AWS access key in the older S3 bucket logs. What is the `AccessKeyId` value that was leaked?

Temporary credentials from assumed roles use Access Key IDs starting with "ASIA". From the previous output, we can see the access key `ASIASFUIRZ5AETONKITQ` was exposed.  
![](../../../../attachments/attachment-awswatcher-lab-05122026-9.png)  

## A critical alert was triggered when the attacker invoked an API to retrieve temporary credentials. What is the Event ID of the `GetRole` API call?

We can search for the `GetRole` API in the `eventName` field to find logs for this event.  
```bash
jq '.Records[] | select(.eventName == "GetRole") | {eventTime: .eventTime, eventId: .eventID}' 149536493376_CloudTrail_us-east-1_20250223T0055Z_d0om30WedJHjcc8O.json
```

The command returned one result at 2025-02-23 00:51:21 with an event ID of `78efd559-c626-4002-b458-088a4cc80e53`.  
![](../../../../attachments/attachment-awswatcher-lab-05122026-10.png)  

## Analysis of HTTP User-Agent strings and CLI artifacts suggests the attacker was using a penetration-testing operating system. Which operating system was likely used by the attacker?

The command below will search for all logs from source IP address `41.46.53.241` and output the event time and user agent.  
```bash
jq '.Records[] | select(.sourceIPAddress == "41.46.53.241") | {eventTime: .eventTime, userAgent: .userAgent}' 149536493376_CloudTrail_us-east-1_20250223T0055Z_d0om30WedJHjcc8O.json
```

Analysis into the result shows an event at 2025-02-23 00:51:21 where the User-Agent revealed usage of the `kali` operating system.  
![](../../../../attachments/attachment-awswatcher-lab-05122026-11.png)  