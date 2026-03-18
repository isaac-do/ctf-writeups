---
date: 2026-03-17
tags:
  - threat-intel
---
# Challenge Overview
---
**Challenge:** [Yellow RAT](https://cyberdefenders.org/blueteam-ctf-challenges/yellow-rat/)  
**Platform:** CyberDefender  
**Category:** Threat Intel  
**Difficulty:** Easy  
**Tools:** VirusTotal, Red Canary  

# Summary
---


# Scenario
---
During a regular IT security check at GlobalTech Industries, abnormal network traffic was detected from multiple workstations. Upon initial investigation, it was discovered that certain employees' search queries were being redirected to unfamiliar websites. This discovery raised concerns and prompted a more thorough investigation. Your task is to investigate this incident and gather as much information as possible.

# Challenge
---
## Understanding the adversary helps defend against attacks. What is the name of the malware family that causes abnormal network traffic?

Upload the malware hash to VirusTotal then navigate to the Relations tab and explore the graph summary.  
What we will find is that there are several associations with the hash, however, the most interesting one that relates to network is Yellow Cockatoo.  
![](../../attachments/attachment-03172026-26.png)  

## As part of our incident response, knowing common filenames the malware uses can help scan other workstations for potential infection. What is the common filename associated with the malware discovered on our workstations?

Navigate to the Details tab, then under the **Signature Info** section we can find the original name of the malware.  
![](../../attachments/attachment-03172026-27.png)  

## Determining the compilation timestamp of malware can reveal insights into its development and deployment timeline. What is the compilation timestamp of the malware that infected our network?


## Understanding when the broader cybersecurity community first identified the malware could help determine how long the malware might have been in the environment before detection. When was the malware first submitted to VirusTotal?


## To completely eradicate the threat from Industries' systems, we need to identify all components dropped by the malware. What is the name of the .dat file that the malware dropped in the AppData folder?


## It is crucial to identify the C2 servers with which the malware communicates to block its communication and prevent further data exfiltration. What is the C2 server that the malware is communicating with?


