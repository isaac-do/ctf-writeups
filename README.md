# CTF Writeups
This is my collection of CTF writeups covering digital forensics, threat detection, exploitation analysis, incident response exercises, and many more. This repository documents the process I used to analyze and solve challenges from various security training platforms. My goal is to provide a clear record of investigation techniques, tools, and reasoning used during each challenge.

## Writeups
Each writeup in this repository provides a step-by-step breakdown of the approach taken to retrieve the challenge flag. The writeups explain the investigation or exploitation process used to solve the challenge, including the tools, commands, and reasoning behind the analysis. Challenges are grouped by their general category, such as DFIR, threat intelligence, and network analysis. The difficulty labels categorized in the writeups follow the ratings provided by the original platform so whatever HackTheBox or TryHackMe labeled as Easy or Hard is what I used.  

| Difficulty | Rating |
|-----|-----|
| Very Easy | ⭐ |
| Easy | ⭐⭐ |
| Medium | ⭐⭐⭐ |
| Hard | ⭐⭐⭐⭐ |
| Insane | ⭐⭐⭐⭐⭐ |

## Table of Contents
- [DFIR](#dfir)
- [Cyber Threat Intelligence (CTI)](#cyber-threat-intelligence-cti)
- [Phishing Analysis](#phishing-analysis)
- [Tools](#tools)

### DFIR
| Name       | Writeup                                   | Challenge                                                                       | Difficulty | Rating | Tags                                            |
| ---------- | ----------------------------------------- | ------------------------------------------------------------------------------- | ---------- | ------ | ----------------------------------------------- |
| Summit     | [Link](writeups/tryhackme/summit.md)      | [TryHackMe](https://tryhackme.com/)                                             | Easy       | ⭐⭐     | `Log Analysis` `MITRE ATT&CK` `Pyramid of Pain` |
| Campfire-2 | [Link](writeups/hackthebox/campfire-2.md) | [HackTheBox](https://app.hackthebox.com/sherlocks/Campfire-2?tab=play_sherlock) | Very Easy  | ⭐      | `Event Viewer`                                  |
| Brutus     | [Link](writeups/hackthebox/brutus.md)     | [HackTheBox](https://app.hackthebox.com/sherlocks/Brutus?tab=play_sherlock)     | Very Easy  | ⭐      | `grep` `cat` `MITRE ATT&CK`                     |

### Cyber Threat Intelligence (CTI)
| Name        | Writeup                                    | Challenge                                                                            | Difficulty | Rating | Tags                        |
| ----------- | ------------------------------------------ | ------------------------------------------------------------------------------------ | ---------- | ------ | --------------------------- |
| Eviction    | [Link](writeups/tryhackme/eviction.md)     | [TryHackMe](https://tryhackme.com/room/eviction)                                     | Easy       | ⭐⭐     | `MITRE ATT&CK`              |
| Dream Job-1 | [Link](writeups/hackthebox/dream_job-1.md) | [HackTheBox](https://app.hackthebox.com/sherlocks/Dream%2520Job-1?tab=play_sherlock) | Easy       | ⭐⭐     | `MITRE ATT&CK` `VirusTotal` |

### Phishing Analysis
| Name                    | Writeup                                               | Challenge                                                                            | Difficulty | Rating | Tags                                                   |
| ----------------------- | ----------------------------------------------------- | ------------------------------------------------------------------------------------ | ---------- | ------ | ------------------------------------------------------ |
| Snapped Phish-ing Line | [Link](writeups/tryhackme/snapped_phish-ing_line.md) | [TryHackMe](https://tryhackme.com/room/snappedphishingline)                         | Easy       | ⭐⭐     | `VirusTotal` `CyberChef` `whois` `grep` |
| The Greenholt Phish | [Link](writeups/tryhackme/the_greenholt_phish.md) | [TryHackMe](https://tryhackme.com/room/phishingemails5fgjlzxc)                         | Easy       | ⭐⭐     | `whois` `VirusTotal` |
| Phishing Analysis Tools | [Link](writeups/tryhackme/phishing_analysis_tools.md) | [TryHackMe](https://tryhackme.com/room/phishingemails3tryoe)                         | Easy       | ⭐⭐     |  `CyberChef` `Any.Run` `Malware Analysis` |

### Tools
| Tool | Category | Link |
|-----|-----|-----|
| MITRE ATT&CK | CTI | https://attack.mitre.org/ |
| VirusTotal | CTI | https://www.virustotal.com/ |
| WhoIs | CTI | https://www.whois.com/whois/ |
| Any.Run | Malware Analysis | https://any.run/ |
| CyberChef | DFIR | https://gchq.github.io/CyberChef/ |
