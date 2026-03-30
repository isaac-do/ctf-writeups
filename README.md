# CTF Writeups
This is my collection of CTF writeups covering digital forensics, threat detection, exploitation analysis, incident response exercises, and many more. This repository documents the process I used to analyze and solve challenges from various security training platforms. My goal is to provide a clear record of investigation techniques, tools, and reasoning used during each challenge.

## Writeups
Each writeup in this repository provides a step-by-step breakdown of the approach taken to retrieve the challenge flag. The writeups explain the investigation process used to solve the challenge, including the tools, commands, and reasoning behind the analysis. Challenges are grouped by their general category, such as DFIR, threat intelligence, and network forensics. The difficulty labels categorized in the writeups follow the ratings provided by the original platform so whatever HackTheBox or TryHackMe labeled as Easy or Hard is what I used.  

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
| Name                  | Writeup                                                                        | Challenge                                                                             | Difficulty | Rating | Tags                           |
| --------------------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- | ---------- | ------ | ------------------------------ |
| Redline Lab           | [Link](writeups/cyberdefenders/endpoint-forensics/easy/redline-lab.md)         | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/redline/)         | Easy       | ⭐⭐     | `Volatility3` `strings`        |
| Ramnit Lab            | [Link](writeups/cyberdefenders/endpoint-forensics/easy/ramnit-lab.md)          | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/ramnit/)          | Easy       | ⭐⭐     | `Volatility3` `VirusTotal`     |
| Insider Lab           | [Link](writeups/cyberdefenders/endpoint-forensics/easy/insider-lab.md)         | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/insider/)         | Easy       | ⭐⭐     | `FTK Imager` `LogViewer2`      |
| Amadey - APT-C-36 Lab | [Link](writeups/cyberdefenders/endpoint-forensics/easy/amadey-apt-c-36-lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/amadey-apt-c-36/) | Easy       | ⭐⭐     | `Volatility3` `grep` `strings` |
| The Crime Lab         | [Link](writeups/cyberdefenders/endpoint-forensics/easy/the-crime-lab.md)       | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/the-crime/)       | Easy       | ⭐⭐     | `ALEAPP`                       |

## Network Forensics
| Name                     | Writeup                                                                           | Challenge                                                                                 | Difficulty | Rating | Tags                     |
| ------------------------ | --------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ---------- | ------ | ------------------------ |
| Tomcat Takeover Lab      | [Link](writeups/cyberdefenders/network-forensics/easy/tomcat-takeover-lab.md)     | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/tomcat-takeover/)     | Easy       | ⭐⭐     | `Wireshark`              |
| PacketDetective Lab      | [Link](writeups/cyberdefenders/network-forensics/easy/packetdetective-lab.md)     | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/packetdetective/)     | Easy       | ⭐⭐     | `Wireshark`              |
| DanaBot Lab              | [Link](writeups/cyberdefenders/network-forensics/easy/danabot-lab.md)             | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/danabot/)             | Easy       | ⭐⭐     | `Wireshark` `VirusTotal` |
| PsExec Hunt Lab          | [Link](writeups/cyberdefenders/network-forensics/easy/psexec-hunt-lab.md)         | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/psexec-hunt/)         | Easy       | ⭐⭐     | `Wireshark`              |
| Poisoned Credentials Lab | [Link](writeups/cyberdefenders/network-forensics/easy/poisonedcredentials-lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/poisonedcredentials/) | Easy       | ⭐⭐     | `Wireshark`              |

### DFIR
| Name       | Writeup                                   | Challenge                                                                       | Difficulty | Rating | Tags                                            |
| ---------- | ----------------------------------------- | ------------------------------------------------------------------------------- | ---------- | ------ | ----------------------------------------------- |
| Summit     | [Link](writeups/tryhackme/summit.md)      | [TryHackMe](https://cyberdefenders.org/blueteam-ctf-challenges/poisonedcredentials/) | Easy | ⭐⭐     | `MITRE ATT&CK` `Pyramid of Pain` |
| Campfire-2 | [Link](writeups/hackthebox/dfir/very-easy/campfire-2.md) | [HackTheBox](https://app.hackthebox.com/sherlocks/Campfire-2?tab=play_sherlock) | Very Easy  | ⭐      | `Event Viewer` |
| Brutus     | [Link](writeups/hackthebox/dfir/very-easy/brutus.md)     | [HackTheBox](https://app.hackthebox.com/sherlocks/Brutus?tab=play_sherlock)     | Very Easy  | ⭐      | `grep` `cat` `MITRE ATT&CK` |

### Cyber Threat Intelligence (CTI)
| Name                 | Writeup                                                                   | Challenge                                                                              | Difficulty | Rating | Tags                                     |
| -------------------- | ------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | ---------- | ------ | ---------------------------------------- |
| IceID Lab            | [Link](writeups/cyberdefenders/threat-intel/easy/iceid-lab.md)            | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/icedid/)           | Easy       | ⭐⭐     | `VirusTotal` `MITRE ATT&CK`              |
| GrabThePhisher Lab   | [Link](writeups/cyberdefenders/threat-intel/easy/grabthephisher-lab.md)   | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/grabthephisher/)   | Easy       | ⭐⭐     | `VSCode`                                 |
| 3CX Supply Chain Lab | [Link](writeups/cyberdefenders/threat-intel/easy/3cx-supply-chain-lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/3cx-supply-chain/) | Easy       | ⭐⭐     | `VirusTotal` `MITRE ATT&CK`              |
| Red Stealer Lab      | [Link](writeups/cyberdefenders/threat-intel/easy/red-stealer-lab.md)      | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/red-stealer/)      | Easy       | ⭐⭐     | `VirusTotal` `MalwareBazaar` `ThreatFox` |
| Yellow RAT Lab       | [Link](writeups/cyberdefenders/threat-intel/easy/yellow-rat-lab.md)       | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/yellow-rat/)       | Easy       | ⭐⭐     | `VirusTotal`                             |
| Oski Lab             | [Link](writeups/cyberdefenders/threat-intel/easy/oski-lab.md)             | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/oski/)             | Easy       | ⭐⭐     | `MITRE ATT&CK` `VirusTotal` `Any.Run`    |
| Eviction             | [Link](writeups/tryhackme/eviction.md)                                    | [TryHackMe](https://tryhackme.com/room/eviction)                                       | Easy       | ⭐⭐     | `MITRE ATT&CK`                           |
| Dream Job-1          | [Link](writeups/hackthebox/threat-intel/very-easy/dream-job-1.md)         | [HackTheBox](https://app.hackthebox.com/sherlocks/Dream%2520Job-1?tab=play_sherlock)   | Easy       | ⭐⭐     | `MITRE ATT&CK` `VirusTotal`              |

### Open-Source Intelligence (OSINT)
| Name        | Writeup                                    | Challenge                                                                            | Difficulty | Rating | Tags                        |
| ----------- | ------------------------------------------ | ------------------------------------------------------------------------------------ | ---------- | ------ | --------------------------- |
| Lespion Lab | [Link](writeups/cyberdefenders/threat-intel/easy/lespion-lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/lespion/)     | Easy       | ⭐⭐     | `Google Images search` `CyberChef` |
| Dev Diaries    | [Link](writeups/tryhackme/dev_diaries.md)     | [TryHackMe](https://tryhackme.com/room/devdiaries) | Easy | ⭐⭐     | `pentesting-tools` `GitHub` |
| Missing Person | [Link](writeups/tryhackme/missing_person.md) | [TryHackMe](https://tryhackme.com/room/missingperson) | Easy | ⭐⭐     | `Google Images search` `exifmeta` |

### Phishing Analysis
| Name                    | Writeup                                               | Challenge                                                                            | Difficulty | Rating | Tags                                                   |
| ----------------------- | ----------------------------------------------------- | ------------------------------------------------------------------------------------ | ---------- | ------ | ------------------------------------------------------ |
| Snapped Phish-ing Line | [Link](writeups/tryhackme/snapped_phish-ing_line.md) | [TryHackMe](https://tryhackme.com/room/snappedphishingline) | Easy       | ⭐⭐     | `VirusTotal` `CyberChef` `whois` `grep` |
| The Greenholt Phish | [Link](writeups/tryhackme/the_greenholt_phish.md) | [TryHackMe](https://tryhackme.com/room/phishingemails5fgjlzxc) | Easy       | ⭐⭐     | `whois` `VirusTotal` |
| Phishing Analysis Tools | [Link](writeups/tryhackme/phishing_analysis_tools.md) | [TryHackMe](https://tryhackme.com/room/phishingemails3tryoe) | Easy       | ⭐⭐     |  `CyberChef` `Any.Run` |

### Tools
| Tool         | Category           | Link                                                                                                                           |
| ------------ | ------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| LogViewer2   | Endpoint Forensics | [https://github.com/woanware/LogViewer2](https://github.com/woanware/LogViewer2)                                               |
| FTK Imager   | Endpoint Forensics | [https://www.exterro.com/digital-forensics-software/ftk-imager](https://www.exterro.com/digital-forensics-software/ftk-imager) |
| Volatility3  | Endpoint Forensics | https://github.com/volatilityfoundation/volatility3                                                                            |
| ALEAPP       | Endpoint Forensics | https://github.com/abrignoni/ALEAPP                                                                                            |
| Wireshark    | Network Forensics  | https://www.wireshark.org/                                                                                                     |
| MITRE ATT&CK | CTI                | https://attack.mitre.org/                                                                                                      |
| VirusTotal   | CTI                | https://www.virustotal.com/                                                                                                    |
| WhoIs        | CTI                | https://www.whois.com/whois/                                                                                                   |
| Any.Run      | Malware Analysis   | https://any.run/                                                                                                               |
| CyberChef    | DFIR               | https://gchq.github.io/CyberChef/                                                                                              |
| ExifMeta     | OSINT              | https://exifmeta.com/                                                                                                          |
