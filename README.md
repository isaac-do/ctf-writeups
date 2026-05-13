# CTF Writeups
This is my collection of CTF writeups focused on blue team and DFIR disciplines, including memory and disk forensics, network traffic analysis, threat hunting, cloud forensics, and more. All challenges are sourced from platforms like CyberDefenders, HackTheBox Sherlocks, and TryHackMe. My goal is to provide a clear record of investigation techniques, tools, and reasoning used during each challenge.  

## Writeups
Each writeup in this repository provides a step-by-step breakdown of the approach taken to answer each challenge question. The writeups explain the investigation process, including the tools, commands, and reasoning behind the analysis. Challenges are grouped by their general category, such as endpoint forensics, network forensics, threat hunting, etc. The difficulty labels categorized in the writeups follow the ratings provided by the original platform so whatever HackTheBox or TryHackMe labeled as Easy or Hard is what I used.  

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
- [Threat Hunting](#threat-hunting)
- [Cloud Forensics](#cloud-forensics)
- [DFIR](#dfir)
- [Cyber Threat Intelligence (CTI)](#cyber-threat-intelligence-cti)
- [Open-Source Intelligence (OSINT)](#open-source-intelligence-osint)
- [Phishing Analysis](#phishing-analysis)
- [Tools](#tools)

## Endpoint Forensics
| Name                               | Writeup                                                                                | Challenge                                                                                          | Difficulty | Rating | Tags                                                              |
| ---------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | ---------- | ------ | ----------------------------------------------------------------- |
| T1598.002 - Dragonfly Lab          | [Link](writeups/cyberdefenders/endpoint-forensics/easy/t1598-002-dragonfly-lab.md)     | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/t1598002-dragonfly/)           | Easy       | ⭐⭐     | `oledump`                                                         |
| Fork Bomb - TeamPCP Lab            | HIDDEN (Active Lab)                                                                    | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/fork-bomb-teampcp/)            | Easy       | ⭐⭐     | `Notepad++` `Sysmon`                                              |
| ContainerBreak - Rootkit Trail Lab | HIDDEN (Active Lab)                                                                    | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/containerbreak-rootkit-trail/) | Easy       | ⭐⭐     | `Linux Commnand Lines`                                            |
| MeteorHit - Indra Lab              | [Link](writeups/cyberdefenders/endpoint-forensics/medium/meteorhit-indra-lab.md)       | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/meteorhit-indra/)              | Medium     | ⭐⭐⭐    | `Registry Explorer` `Event Log Explorer`                          |
| Andromeda Bot - UNC4210 Lab        | [Link](writeups/cyberdefenders/endpoint-forensics/medium/andromeda-bot-unc4210-lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/andromeda-bot-unc4210/)        | Medium     | ⭐⭐⭐    | `MemProcFS` `EvtxECmd` `Timeline Explorer` `VirusTotal` `ANY.RUN` |
| XMRig Lab                          | [Link](writeups/cyberdefenders/endpoint-forensics/medium/xmrig-lab.md)                 | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/xmrig/)                        | Medium     | ⭐⭐⭐    | `Photorec` `losetup` `strings` `mount` `ANY.RUN`                  |
| Volatility Traces Lab              | [Link](writeups/cyberdefenders/endpoint-forensics/easy/volatility-traces-lab.md)       | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/volatility-traces/)            | Easy       | ⭐⭐     | `Volatility3`                                                     |
| AndroidBreach Lab                  | [Link](writeups/cyberdefenders/endpoint-forensics/medium/androidbreach-lab.md)         | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/androidbreach/)                | Medium     | ⭐⭐⭐    | `ALEAPP` `jadx` `CyberChef` `DB Browser for SQLite`               |
| Reveal Lab                         | [Link](writeups/cyberdefenders/endpoint-forensics/easy/reveal-lab.md)                  | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/reveal/)                       | Easy       | ⭐⭐     | `Volatility3`                                                     |
| Redline Lab                        | [Link](writeups/cyberdefenders/endpoint-forensics/easy/redline-lab.md)                 | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/redline/)                      | Easy       | ⭐⭐     | `Volatility3` `strings` `awk`                                     |
| Ramnit Lab                         | [Link](writeups/cyberdefenders/endpoint-forensics/easy/ramnit-lab.md)                  | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/ramnit/)                       | Easy       | ⭐⭐     | `Volatility3` `VirusTotal`                                        |
| Insider Lab                        | [Link](writeups/cyberdefenders/endpoint-forensics/easy/insider-lab.md)                 | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/insider/)                      | Easy       | ⭐⭐     | `FTK Imager` `LogViewer2`                                         |
| Amadey - APT-C-36 Lab              | [Link](writeups/cyberdefenders/endpoint-forensics/easy/amadey-apt-c-36-lab.md)         | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/amadey-apt-c-36/)              | Easy       | ⭐⭐     | `Volatility3` `grep` `strings`                                    |
| The Crime Lab                      | [Link](writeups/cyberdefenders/endpoint-forensics/easy/the-crime-lab.md)               | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/the-crime/)                    | Easy       | ⭐⭐     | `ALEAPP`                                                          |

## Network Forensics
| Name                            | Writeup                                                                           | Challenge                                                                                       | Difficulty | Rating | Tags                                                   |
| ------------------------------- | --------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ---------- | ------ | ------------------------------------------------------ |
| CallMeOnTheChain - EtherRAT Lab | HIDDEN (Active Lab)                                                               | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/callmeonthechain-etherrat/) | Medium     | ⭐⭐⭐    | `Wireshark`                                            |
| RediShell - Kinsing Lab         | HIDDEN (Active Lab)                                                               | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/redishell-kinsing/)         | Easy       | ⭐⭐     | `Wireshark`                                            |
| XXE Infiltration Lab            | [Link](writeups/cyberdefenders/network-forensics/easy/xxe-infiltration-lab.md)    | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/xxe-infiltration/)          | Easy       | ⭐⭐     | `Wireshark`                                            |
| RetailBreach Lab                | [Link](writeups/cyberdefenders/network-forensics/easy/retailbreach-lab.md)        | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/retailbreach/)              | Easy       | ⭐⭐     | `Wireshark`                                            |
| JetBrains Lab                   | [Link](writeups/cyberdefenders/network-forensics/easy/jetbrains-lab.md)           | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/jetbrains/)                 | Easy       | ⭐⭐     | `Wireshark`                                            |
| Lockdown Lab                    | HIDDEN (Active Lab)                                                               | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/lockdown/)                  | Easy       | ⭐⭐     | `Wireshark` `Volatility3` `VirusTotal` `MalwareBazaar` |
| XLMRat Lab                      | HIDDEN<br>(Active Lab)                                                            | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/xlmrat/)                    | Easy       | ⭐⭐     | `Wireshark` `CyberChef` `VirusTotal`                   |
| Web Investigation Lab           | [Link](writeups/cyberdefenders/network-forensics/easy/web-investigation-lab.md)   | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/web-investigation/)         | Easy       | ⭐⭐     | `Wireshark` `CyberChef`                                |
| Tomcat Takeover Lab             | [Link](writeups/cyberdefenders/network-forensics/easy/tomcat-takeover-lab.md)     | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/tomcat-takeover/)           | Easy       | ⭐⭐     | `Wireshark`                                            |
| PacketDetective Lab             | [Link](writeups/cyberdefenders/network-forensics/easy/packetdetective-lab.md)     | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/packetdetective/)           | Easy       | ⭐⭐     | `Wireshark`                                            |
| DanaBot Lab                     | [Link](writeups/cyberdefenders/network-forensics/easy/danabot-lab.md)             | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/danabot/)                   | Easy       | ⭐⭐     | `Wireshark` `VirusTotal`                               |
| PsExec Hunt Lab                 | [Link](writeups/cyberdefenders/network-forensics/easy/psexec-hunt-lab.md)         | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/psexec-hunt/)               | Easy       | ⭐⭐     | `Wireshark`                                            |
| Poisoned Credentials Lab        | [Link](writeups/cyberdefenders/network-forensics/easy/poisonedcredentials-lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/poisonedcredentials/)       | Easy       | ⭐⭐     | `Wireshark`                                            |

## Threat Hunting

| Name                        | Writeup                                                                          | Challenge                                                                                   | Difficulty | Rating | Tags                  |
| --------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ---------- | ------ | --------------------- |
| FalconEye Lab               | [Link](writeups/cyberdefenders/threat-hunting/medium/falconeye-lab.md)           | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/falconeye/)             | Medium     | ⭐⭐⭐    | `Splunk`              |
| Kerberoasted Lab            | [Link](writeups/cyberdefenders/threat-hunting/medium/kerberoasted-lab.md)        | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/kerberoasted/)          | Medium     | ⭐⭐⭐    | `Splunk`              |
| T1197 Lab                   | [Link](writeups/cyberdefenders/threat-hunting/medium/t1197-lab.md)               | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/t1197/)                 | Medium     | ⭐⭐⭐    | `Splunk`              |
| T1110-003 Lab               | [Link](writeups/cyberdefenders/threat-hunting/easy/t1110-003-lab.md)             | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/t1110003/)              | Easy       | ⭐⭐     | `Splunk`              |
| Boss Of The SOC v1 Lab      | [Link](writeups/cyberdefenders/threat-hunting/medium/boss-of-the-soc-v1-lab.md)  | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/boss-of-the-soc-v1/)    | Medium     | ⭐⭐⭐    | `Splunk`              |
| ShadowRoast Lab             | [Link](writeups/cyberdefenders/threat-hunting/medium/shadowroast-lab.md)         | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/shadowroast/)           | Medium     | ⭐⭐⭐    | `Splunk`              |
| GoldenSpray Lab             | [Link](writeups/cyberdefenders/threat-hunting/medium/goldenspray-lab.md)         | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/goldenspray/)           | Medium     | ⭐⭐⭐    | `Splunk` `IPinfo`     |
| REvil - GOLD SOUTHFIELD Lab | [Link](writeups/cyberdefenders/threat-hunting/easy/revil-gold-southfield-lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/revil-gold-southfield/) | Easy       | ⭐⭐     | `Splunk` `ANY.RUN`    |
| NerisBot Lab                | [Link](writeups/cyberdefenders/threat-hunting/easy/nerisbot-lab.md)              | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/nerisbot/)              | Easy       | ⭐⭐     | `Splunk` `VirusTotal` |

## Cloud Forensics

| Name                  | Writeup                                                                         | Challenge                                                                               | Difficulty | Rating | Tags                           |
| --------------------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | ---------- | ------ | ------------------------------ |
| DynamicEscalate Lab   | HIDDEN <br>(Active Lab)                                                         | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/dynamicescalate/)   | Easy       | ⭐⭐     | `Microsoft Sentinel`           |
| S3CredentialsHunt Lab | [Link](writeups/cyberdefenders/cloud-forensics/medium/s3credentialshunt-lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/s3credentialshunt/) | Medium     | ⭐⭐⭐    | `jq`                           |
| IMDSv1 Lab            | [Link](writeups/cyberdefenders/cloud-forensics/medium/imdsv1-lab.md)            | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/imdsv1/)            | Medium     | ⭐⭐⭐    | `Wireshark` `jq`               |
| AWSWatcher Lab        | [Link](writeups/cyberdefenders/cloud-forensics/easy/awswatcher-lab.md)          | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/awswatcher/)        | Easy       | ⭐⭐     | `CloudTrail` `CloudWatch` `jq` |
| AzureHunt Lab         | [Link](writeups/cyberdefenders/cloud-forensics/easy/azurehunt-lab.md)           | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/azurehunt/)         | Easy       | ⭐⭐     | `ELK`                          |
| AWSRaid Lab           | [Link](writeups/cyberdefenders/cloud-forensics/easy/awsraid-lab.md)             | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/awsraid/)           | Easy       | ⭐⭐     | `Splunk`                       |

### DFIR
| Name       | Writeup                                   | Challenge                                                                       | Difficulty | Rating | Tags                                            |
| ---------- | ----------------------------------------- | ------------------------------------------------------------------------------- | ---------- | ------ | ----------------------------------------------- |
| Summit     | [Link](writeups/tryhackme/summit.md)      | [TryHackMe](https://cyberdefenders.org/blueteam-ctf-challenges/poisonedcredentials/) | Easy | ⭐⭐     | `MITRE ATT&CK` `Pyramid of Pain` |
| Campfire-2 | [Link](writeups/hackthebox/dfir/very-easy/campfire-2.md) | [HackTheBox](https://app.hackthebox.com/sherlocks/Campfire-2?tab=play_sherlock) | Very Easy  | ⭐      | `Event Viewer` |
| Brutus     | [Link](writeups/hackthebox/dfir/very-easy/brutus.md)     | [HackTheBox](https://app.hackthebox.com/sherlocks/Brutus?tab=play_sherlock)     | Very Easy  | ⭐      | `grep` `cat` `MITRE ATT&CK` |

### Cyber Threat Intelligence (CTI)
| Name                 | Writeup                                                                   | Challenge                                                                              | Difficulty | Rating | Tags                                     |
| -------------------- | ------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | ---------- | ------ | ---------------------------------------- |
| IceID Lab            | [Link](writeups/cyberdefenders/threat-intel/easy/icedid-lab.md)           | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/icedid/)           | Easy       | ⭐⭐     | `VirusTotal` `MITRE ATT&CK`              |
| GrabThePhisher Lab   | [Link](writeups/cyberdefenders/threat-intel/easy/grabthephisher-lab.md)   | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/grabthephisher/)   | Easy       | ⭐⭐     | `VSCode`                                 |
| 3CX Supply Chain Lab | [Link](writeups/cyberdefenders/threat-intel/easy/3cx-supply-chain-lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/3cx-supply-chain/) | Easy       | ⭐⭐     | `VirusTotal` `MITRE ATT&CK`              |
| Red Stealer Lab      | [Link](writeups/cyberdefenders/threat-intel/easy/red-stealer-lab.md)      | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/red-stealer/)      | Easy       | ⭐⭐     | `VirusTotal` `MalwareBazaar` `ThreatFox` |
| Yellow RAT Lab       | [Link](writeups/cyberdefenders/threat-intel/easy/yellow-rat-lab.md)       | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/yellow-rat/)       | Easy       | ⭐⭐     | `VirusTotal`                             |
| Oski Lab             | [Link](writeups/cyberdefenders/threat-intel/easy/oski-lab.md)             | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/oski/)             | Easy       | ⭐⭐     | `MITRE ATT&CK` `VirusTotal` `Any.Run`    |
| Eviction             | [Link](writeups/tryhackme/eviction.md)                                    | [TryHackMe](https://tryhackme.com/room/eviction)                                       | Easy       | ⭐⭐     | `MITRE ATT&CK`                           |
| Dream Job-1          | [Link](writeups/hackthebox/threat-intel/very-easy/dream-job-1.md)         | [HackTheBox](https://app.hackthebox.com/sherlocks/Dream%2520Job-1?tab=play_sherlock)   | Easy       | ⭐⭐     | `MITRE ATT&CK` `VirusTotal`              |

### Open-Source Intelligence (OSINT)
| Name                        | Writeup                                                                   | Challenge                                                                                   | Difficulty | Rating | Tags                                       |
| --------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ---------- | ------ | ------------------------------------------ |
| Tusk Infostealer Lab        | [Link](writeups/cyberdefenders/threat-intel/easy/tusk-infostealer-lab.md) | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/tusk-infostealer/)      | Easy       | ⭐⭐     | `VirusTotal` `Threat Intelligence Reports` |
| RaaS Unfold - RansomHub Lab | HIDDEN<br>(Active Lab)                                                    | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/raas-unfold-ransomhub/) | Medium     | ⭐⭐⭐    | `Threat Intelligence Reports`              |
| Lespion Lab                 | [Link](writeups/cyberdefenders/threat-intel/easy/lespion-lab.md)          | [CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/lespion/)               | Easy       | ⭐⭐     | `Google Images search` `CyberChef`         |
| Dev Diaries                 | [Link](writeups/tryhackme/dev_diaries.md)                                 | [TryHackMe](https://tryhackme.com/room/devdiaries)                                          | Easy       | ⭐⭐     | `pentesting-tools` `GitHub`                |
| Missing Person              | [Link](writeups/tryhackme/missing_person.md)                              | [TryHackMe](https://tryhackme.com/room/missingperson)                                       | Easy       | ⭐⭐     | `Google Images search` `exifmeta`          |

### Phishing Analysis
| Name                    | Writeup                                               | Challenge                                                                            | Difficulty | Rating | Tags                                                   |
| ----------------------- | ----------------------------------------------------- | ------------------------------------------------------------------------------------ | ---------- | ------ | ------------------------------------------------------ |
| Snapped Phish-ing Line | [Link](writeups/tryhackme/snapped_phish-ing_line.md) | [TryHackMe](https://tryhackme.com/room/snappedphishingline) | Easy       | ⭐⭐     | `VirusTotal` `CyberChef` `whois` `grep` |
| The Greenholt Phish | [Link](writeups/tryhackme/the_greenholt_phish.md) | [TryHackMe](https://tryhackme.com/room/phishingemails5fgjlzxc) | Easy       | ⭐⭐     | `whois` `VirusTotal` |
| Phishing Analysis Tools | [Link](writeups/tryhackme/phishing_analysis_tools.md) | [TryHackMe](https://tryhackme.com/room/phishingemails3tryoe) | Easy       | ⭐⭐     |  `CyberChef` `Any.Run` |

### Tools
| Tool         | Category           | Link                                                                                                                           |
| ------------ | ------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| Splunk       | Threat Hunting     | [https://www.splunk.com/](https://www.splunk.com/)                                                                             |
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
