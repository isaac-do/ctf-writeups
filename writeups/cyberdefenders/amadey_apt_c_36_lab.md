---
date: 2026-03-23
tags:
  - dfir
  - cyberdefenders
  - volatility
  - endpoint-forensics
---
# Lab Overview
---
**Lab:** [Amadey - APT-C-36 Lab](https://cyberdefenders.org/blueteam-ctf-challenges/amadey-apt-c-36/)  
**Platform:** CyberDefenders  
**Category:** Endpoint Forensics  
**Difficulty:** Easy  
**Tools:** Volatility3

# Summary
---
Write a summary of the CTF challenge.

# Scenario
---
An after-hours alert from the Endpoint Detection and Response (EDR) system flags suspicious activity on a Windows workstation. The flagged malware aligns with the Amadey Trojan Stealer. Your job is to analyze the presented memory dump and create a detailed report for actions taken by the malware.

# Background
---
Write a short background detailing the attack, indicators, and how to identify.

# Analysis
---
## In the memory dump analysis, determining the root of the malicious activity is essential for comprehending the extent of the intrusion. What is the name of the parent process that triggered this malicious behavior?


## Once the rogue process is identified, its exact location on the device can reveal more about its nature and source. Where is this process housed on the workstation?


## Persistent external communications suggest the malware's attempts to reach out C2C server. Can you identify the Command and Control (C2C) server IP that the process interacts with?


## Following the malware link with the C2C, the malware is likely fetching additional tools or modules. How many distinct files is it trying to bring onto the compromised workstation?


## Identifying the storage points of these additional components is critical for containment and cleanup. What is the full path of the file downloaded and used by the malware in its malicious activity?


## Once retrieved, the malware aims to activate its additional components. Which child process is initiated by the malware to execute these files?


## Understanding the full range of Amadey's persistence mechanisms can help in an effective mitigation. Apart from the locations already spotlighted, where else might the malware be ensuring its consistent presence?

