---
date: 2026-03-12
tags:
  - tryhackme
  - phishing-analysis
---
# Challenge Overview
---
**Challenge:** [Phishing Analysis Tools](https://tryhackme.com/room/phishingemails3tryoe)
**Platform:** TryHackMe  
**Category:** Phishing Analysis  
**Difficulty:** Easy  
**Tools Used:** Any.Run, CyberChef, Google Messageheader

# Summary
---
This room teaches how to investigate phishing emails using common analysis tools and techniques. It focuses on extracting key information from email headers, analyzing suspicious links and attachments, and using threat-intelligence services to verify domains, IP addresses, and files. The goal is to develop practical skills for identifying phishing indicators and conducting basic email threat investigations.

# Scenario
---
You are a Level 1 SOC Analyst. Several suspicious emails have been forwarded to you from other coworkers. You must obtain details from each email for your team to implement the appropriate rules to prevent colleagues from receiving additional spam/phishing emails. 

# Challenge
---
## Phishing Case 1
### What brand was this email tailored to impersonate?
![](../../attachments/attachment-03132026.png)  

### What is the From email address?
![](../../attachments/attachment-03132026-1.png)  

### What is the originating IP? Defang the IP address. 
![](../../attachments/attachment-03132026-2.png)  
![](../../attachments/attachment-03132026-3.png)  
Copy the header from the email message source.

![](../../attachments/attachment-03132026-4.png)  
Paste the copied email header into [Messageheader](https://toolbox.googleapps.com/apps/messageheader/analyzeheader) tool and run the analysis.

### From what you can gather, what do you think will be a domain of interest? Defang the domain.
Copy the entire email message source then head over to [Cyberchef](https://cyberchef.org).

![](../../attachments/attachment-03132026-5.png)  
Paste in the contents of the email message and use the Extract Domains operation.

### What is the shortened URL? Defang the URL.
![](../../attachments/attachment-03132026-6.png)  
Hover your mouse (DO NOT CLICK) over the Update Account Now button to retrieve the shortened URL.

## Phishing Case 2
Link: [https://app.any.run/tasks/8bfd4c58-ec0d-4371-bfeb-52a334b69f59](https://app.any.run/tasks/8bfd4c58-ec0d-4371-bfeb-52a334b69f59)

### What does AnyRun classify this email as?
![](../../attachments/attachment-03122026-47.png)  

### What is the name of the PDF file?
![](../../attachments/attachment-03122026-48.png)  

### What is the SHA 256 hash for the PDF file?
![](../../attachments/attachment-03122026-49.png)  

### What two IP addresses are classified as malicious? Defang the IP addresses. (answer: IP_ADDR,IP_ADDR)
![](../../attachments/attachment-03122026-50.png)  
![](../../attachments/attachment-03122026-51.png)  

### What Windows process was flagged as Potentially Bad Traffic?
![](../../attachments/attachment-03122026-52.png)  

## Phishing Case 3
Link: [https://app.any.run/tasks/82d8adc9-38a0-4f0e-a160-48a5e09a6e83](https://app.any.run/tasks/82d8adc9-38a0-4f0e-a160-48a5e09a6e83)

### What is this analysis classified as?
![](../../attachments/attachment-03122026-53.png)  

### What is the name of the Excel file?
![](../../attachments/attachment-03122026-54.png)  

### What is the SHA 256 hash for the file?
![](../../attachments/attachment-03122026-55.png)  

### What domains are listed as malicious? Defang the URLs & submit answers in alphabetical order. (answer: URL1,URL2,URL3)
![](../../attachments/attachment-03122026-57.png)  

### What IP addresses are listed as malicious? Defang the IP addresses & submit answers from lowest to highest. (answer: IP1,IP2,IP3)
![](../../attachments/attachment-03122026-58.png)  

### What vulnerability does this malicious attachment attempt to exploit?
![](../../attachments/attachment-03122026-56.png)  