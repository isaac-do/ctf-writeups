---
date: 2026-03-12
tags:
  - mitre
  - tryhackme
  - threat-intelligence
---
# Challenge Overview
---
**Challenge:** [Eviction](https://tryhackme.com/room/eviction)  
**Platform:** TryHackMe  
**Category:** Cyber Threat Intelligence  
**Difficulty:** Easy  
**Tools Used:** MITRE ATT&CK  

# Summary
---
This lab focuses on investigating the tactics and techniques used by the threat group APT28 by tracing their activity through the MITRE ATT&CK framework. The investigation analyzes how the attackers progress through different stages of the attack lifecycle from initial access to command and control and persistence. By mapping observed behaviors and indicators to ATT&CK techniques, the lab demonstrates the methods used by APT28 during an intrusion.

# Scenario
---
Sunny is a SOC analyst at E-corp, which manufactures rare earth metals for government and non-government clients. She receives a classified intelligence report that informs her that an APT group (APT28) might be trying to attack organizations similar to E-corp. To act on this intelligence, she must use the MITRE ATT&CK Navigator to identify the TTPs used by the APT group, to ensure it has not already intruded into the network, and to stop it if it has.

# Challenge
---
## What is a technique used by the APT to both perform recon and gain initial access?
![](../../attachments/attachment-03122026.png)

## Sunny identified that the APT might have moved forward from the recon phase. Which accounts might the APT compromise while developing resources?
![](../../attachments/attachment-03122026-1.png)

## E-corp has found that the APT might have gained initial access using social engineering to make the user execute code for the threat actor. Sunny wants to identify if the APT was also successful in execution. What two techniques of user execution should Sunny look out for? (Answer format: <technique 1> and <technique 2>)
![](../../attachments/attachment-03122026-2.png)

## If the above technique was successful, which scripting interpreters should Sunny search for to identify successful execution? (Answer format: <technique 1> and <technique 2>)
![](../../attachments/attachment-03122026-3.png)


## While looking at the scripting interpreters identified in Q4, Sunny found some obfuscated scripts that changed the registry. Assuming these changes are for maintaining persistence, which registry keys should Sunny observe to track these changes?
![](../../attachments/attachment-03122026-4.png)

## Sunny identified that the APT executes system binaries to evade defences. Which system binary's execution should Sunny scrutinize for proxy execution?
![](../../attachments/attachment-03122026-5.png)
![](../../attachments/attachment-03122026-6.png)
Under Defense Evasion tactic, scroll down to System Binary Proxy Execution.

## Sunny identified tcpdump on one of the compromised hosts. Assuming this was placed there by the threat actor, which technique might the APT be using here for discovery?
![](../../attachments/attachment-03122026-7.png)

## It looks like the APT achieved lateral movement by exploiting remote services. Which remote services should Sunny observe to identify APT activity traces?
![](../../attachments/attachment-03122026-8.png)

## It looked like the primary goal of the APT was to steal intellectual property from E-corp's information repositories. Which information repository can be the likely target of the APT?
![](../../attachments/attachment-03122026-9.png)

## Although the APT had collected the data, it could not connect to the C2 for data exfiltration. To thwart any attempts to do that, what types of proxy might the APT use? (Answer format: <technique 1> and <technique 2>)
![](../../attachments/attachment-03122026-10.png)
