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
- [Endpoint Forensics](#endpoint-forensics)
- [Network Forensics](#network-forensics)
- [DFIR](#dfir)
- [Cyber Threat Intelligence (CTI)](#cyber-threat-intelligence-cti)
- [Open-Source Intelligence (OSINT)](#open-source-intelligence-osint)
- [Phishing Analysis](#phishing-analysis)
- [Tools](#tools)

## Endpoint Forensics
| Name       | Writeup                                   | Challenge                                                                       | Difficulty | Rating | Tags                                            |
| ---------- | ----------------------------------------- | ------------------------------------------------------------------------------- | ---------- | ------ | ----------------------------------------------- |
| Amadey - APT-C-36 Lab     | [Link](writeups/cyberdefenders/amadey_apt_c_36_lab.md)      | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/amadey-apt-c-36/) | Easy | ⭐⭐     | `Volatility3` |
| The Crime Lab     | [Link](writeups/cyberdefenders/the_crime_lab.md)      | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/the-crime/) | Easy | ⭐⭐     | `ALEAPP` |

## Network Forensics
| Name       | Writeup                                   | Challenge                                                                       | Difficulty | Rating | Tags                                            |
| ---------- | ----------------------------------------- | ------------------------------------------------------------------------------- | ---------- | ------ | ----------------------------------------------- |
| Poisoned Credentials Lab     | [Link](writeups/cyberdefenders/poisonedcredentials_lab.md)      | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/poisonedcredentials/) | Easy | ⭐⭐     | `Wireshark` |

### DFIR
| Name       | Writeup                                   | Challenge                                                                       | Difficulty | Rating | Tags                                            |
| ---------- | ----------------------------------------- | ------------------------------------------------------------------------------- | ---------- | ------ | ----------------------------------------------- |
| Summit     | [Link](writeups/tryhackme/summit.md)      | [TryHackMe](https://cyberdefenders.org/blueteam-ctf-challenges/poisonedcredentials/) | Easy | ⭐⭐     | `MITRE ATT&CK` `Pyramid of Pain` |
| Campfire-2 | [Link](writeups/hackthebox/campfire-2.md) | [HackTheBox](https://app.hackthebox.com/sherlocks/Campfire-2?tab=play_sherlock) | Very Easy  | ⭐      | `Event Viewer` |
| Brutus     | [Link](writeups/hackthebox/brutus.md)     | [HackTheBox](https://app.hackthebox.com/sherlocks/Brutus?tab=play_sherlock)     | Very Easy  | ⭐      | `grep` `cat` `MITRE ATT&CK` |

### Cyber Threat Intelligence (CTI)
| Name           | Writeup                                           | Challenge                                                                            | Difficulty | Rating | Tags                                  |
| -------------- | ------------------------------------------------- | ------------------------------------------------------------------------------------ | ---------- | ------ | ------------------------------------- |
| Red Stealer Lab | [Link](writeups/cyberdefenders/red_stealer_lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/red-stealer/)     | Easy       | ⭐⭐     | `VirusTotal` `MalwareBazaar` `ThreatFox` |
| Yellow RAT Lab | [Link](writeups/cyberdefenders/yellow_rat_lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/yellow-rat/)     | Easy       | ⭐⭐     | `VirusTotal`                          |
| Oski Lab       | [Link](writeups/cyberdefenders/oski_lab.md)       | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/oski/)           | Easy       | ⭐⭐     | `MITRE ATT&CK` `VirusTotal` `Any.Run` |
| Eviction       | [Link](writeups/tryhackme/eviction.md)            | [TryHackMe](https://tryhackme.com/room/eviction)                                     | Easy       | ⭐⭐     | `MITRE ATT&CK`                        |
| Dream Job-1    | [Link](writeups/hackthebox/dream_job-1.md)        | [HackTheBox](https://app.hackthebox.com/sherlocks/Dream%2520Job-1?tab=play_sherlock) | Easy       | ⭐⭐     | `MITRE ATT&CK` `VirusTotal`           |

### Open-Source Intelligence (OSINT)
| Name        | Writeup                                    | Challenge                                                                            | Difficulty | Rating | Tags                        |
| ----------- | ------------------------------------------ | ------------------------------------------------------------------------------------ | ---------- | ------ | --------------------------- |
| Lespion Lab | [Link](writeups/cyberdefenders/lespion_lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/lespion/)     | Easy       | ⭐⭐     | `Google Images search` `CyberChef` |
| Dev Diaries    | [Link](writeups/tryhackme/dev_diaries.md)     | [TryHackMe](https://tryhackme.com/room/devdiaries) | Easy | ⭐⭐     | `pentesting-tools` `GitHub` |
| Missing Person | [Link](writeups/tryhackme/missing_person.md) | [TryHackMe](https://tryhackme.com/room/missingperson) | Easy | ⭐⭐     | `Google Images search` `exifmeta` |

### Phishing Analysis
| Name                    | Writeup                                               | Challenge                                                                            | Difficulty | Rating | Tags                                                   |
| ----------------------- | ----------------------------------------------------- | ------------------------------------------------------------------------------------ | ---------- | ------ | ------------------------------------------------------ |
| Snapped Phish-ing Line | [Link](writeups/tryhackme/snapped_phish-ing_line.md) | [TryHackMe](https://tryhackme.com/room/snappedphishingline) | Easy       | ⭐⭐     | `VirusTotal` `CyberChef` `whois` `grep` |
| The Greenholt Phish | [Link](writeups/tryhackme/the_greenholt_phish.md) | [TryHackMe](https://tryhackme.com/room/phishingemails5fgjlzxc) | Easy       | ⭐⭐     | `whois` `VirusTotal` |
| Phishing Analysis Tools | [Link](writeups/tryhackme/phishing_analysis_tools.md) | [TryHackMe](https://tryhackme.com/room/phishingemails3tryoe) | Easy       | ⭐⭐     |  `CyberChef` `Any.Run` |

### Tools
| Tool | Category | Link |
|-----|-----|-----|
| Wireshark | Network Forensics | https://www.wireshark.org/ |
| MITRE ATT&CK | CTI | https://attack.mitre.org/ |
| VirusTotal | CTI | https://www.virustotal.com/ |
| WhoIs | CTI | https://www.whois.com/whois/ |
| Any.Run | Malware Analysis | https://any.run/ |
| CyberChef | DFIR | https://gchq.github.io/CyberChef/ |
| ExifMeta | OSINT | https://exifmeta.com/ |
