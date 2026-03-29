---
date: 2026-03-29
tags:
  - cyberdefenders
  - network-forensics
  - wireshark
---
# Lab Overview
---
**Lab:** [PacketDetective Lab](https://cyberdefenders.org/blueteam-ctf-challenges/packetdetective/)  
**Platform:** CyberDefenders  
**Category:** Network Forensics  
**Difficulty:** Easy  
**Tools:** Wireshark  

# Summary
---
Write a summary of the CTF challenge.

# Scenario
---
In September 2020, your SOC detected suspicious activity from a user device, flagged by unusual SMB protocol usage. Initial analysis indicates a possible compromise of a privileged account and remote access tool usage by an attacker.

Your task is to examine network traffic in the provided PCAP files to identify key indicators of compromise (IOCs) and gain insights into the attacker’s methods, persistence tactics, and goals. Construct a timeline to better understand the progression of the attack by addressing the following questions.

# Analysis
---
## Traffic-1.pcapng

### The attacker’s activity showed extensive SMB protocol usage, indicating a potential pattern of significant data transfer or file access. What is the total number of bytes of the SMB protocol?


### Authentication through SMB was a critical step in gaining access to the targeted system. Identifying the username used for this authentication will help determine if a privileged account was compromised. Which username was utilized for authentication via SMB?


### During the attack, the adversary accessed certain files. Identifying which files were accessed can reveal the attacker's intent. What is the name of the file that was opened by the attacker?


### Clearing event logs is a common tactic to hide malicious actions and evade detection. Pinpointing the timestamp of this action is essential for building a timeline of the attacker’s behavior. What is the timestamp of the attempt to clear the event log? (24-hour UTC format)



## Traffic-2.pcapng

### The attacker used "named pipes" for communication, suggesting they may have utilized Remote Procedure Calls (RPC) for lateral movement across the network. RPC allows one program to request services from another remotely, which could grant the attacker unauthorized access or control. What is the name of the service that communicated using this named pipe?


### Measuring the duration of suspicious communication can reveal how long the attacker maintained unauthorized access, providing insights into the scope and persistence of the attack. What was the duration of communication between the identified addresses 172.16.66.1 and 172.16.66.36?



## Traffic-3.pcapng

### The attacker used a non-standard username to set up requests, indicating an attempt to maintain covert access. Identifying this username is essential for understanding how persistence was established. Which username was used to set up these potentially suspicious requests?


### The attacker leveraged a specific executable file to execute processes remotely on the compromised system. Recognizing this file name can assist in pinpointing the tools used in the attack. What is the name of the executable file utilized to execute processes remotely?