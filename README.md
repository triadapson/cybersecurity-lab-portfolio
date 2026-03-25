# 🛡️ Cybersecurity Lab Portfolio

> **Hands-on lab work across 9 cybersecurity courses — 95+ labs, 400+ exercises**

This repository documents a comprehensive cybersecurity education journey covering everything from hardware fundamentals and network administration through ethical hacking, digital forensics, and cloud security. Each course folder contains detailed lab writeups with objectives, tools used, key findings, and reflections.

---

## 📋 Course Index

| # | Course | Labs | Cert Alignment | README |
|---|--------|------|---------------|--------|
| 1 | [Computer & Networking Fundamentals](#1-computer--networking-fundamentals) | 9 | CompTIA A+ | [View →](./README.md) |
| 2 | [Windows Administration & PowerShell](#2-windows-administration--powershell-scripting) | 9 (86 exercises) | MD-102 | [View →](./Windows_Admin_PowerShell_README.md) |
| 3 | [Windows Server & Directory Administration](#3-windows-server--directory-administration) | 12 | AZ-800 | [View →](./Windows_Server_Directory_Admin_README.md) |
| 4 | [Network+ Labs](#4-network-labs) | 10 | CompTIA N10-008 | [View →](./Network_Plus_Labs_README.md) |
| 5 | [Linux Administration](#5-linux-administration) | 12 | LPIC-1 | [View →](./Linux_Administration_Labs_README.md) |
| 6 | [Cisco Technologies (CCNA)](#6-cisco-technologies-ccna) | 14 | Cisco 200-301 | [View →](./Cisco_CCNA_Labs_README.md) |
| 7 | [Security+ Labs](#7-security-labs) | 7 sections | CompTIA SY0-701 | [View →](./Security_Plus_Labs_README.md) |
| 8 | [Ethical Hacking](#8-ethical-hacking) | 12 | CEH / PenTest+ | [View →](./Ethical_Hacking_Labs_README.md) |
| 9 | [IT Security Forensics](#9-it-security-forensics) | 10 | EC-Council CHFI | [View →](./IT_Security_Forensics_README.md) |

---

## 1. Computer & Networking Fundamentals

**Cert Alignment:** CompTIA A+ (220-1101 / 220-1102) &nbsp;|&nbsp; **Labs:** 9

Foundation course covering the essentials of IT support — from identifying physical hardware components to applying a systematic troubleshooting methodology.

| Lab | Title | Key Topics |
|-----|-------|------------|
| Lab 1 | Hardware & Components | Motherboard, CPU, RAM (DDR3/4/5), storage (HDD/SSD/NVMe), ports, PSU connectors, expansion cards |
| Lab 2 | Network Topology | Bus/Star/Ring/Mesh topologies, LAN/WAN/MAN, Cat5e/Cat6/fibre cables, 802.11ax (Wi-Fi 6), network devices |
| Lab 3 | TCP/IP & Networking Fundamentals | IPv4/IPv6, subnetting, common ports & protocols table (HTTP/HTTPS/SSH/DNS/DHCP/RDP), OSI model, TCP vs UDP |
| Lab 4 | Operating System Fundamentals | Windows CLI (dir, cd, copy), Linux CLI (ls, grep, ps, top), macOS Terminal, Task Manager, Device Manager |
| Lab 5 | Security Concepts | Malware types, social engineering attacks, authentication factors, MFA, encryption (symmetric/asymmetric), CIA triad |
| Lab 6 | Troubleshooting Methodology | CompTIA 6-step model: Identify → Theory → Test → Plan → Verify → Document. 5 real scenarios practised |
| Lab 7 | IT Policies & Procedures | AUP, change management, data classification, BYOD, incident response lifecycle, GDPR/HIPAA/PCI-DSS |
| Lab 8 | Scripting & Automation Basics | Batch files (.bat), PowerShell cmdlets (Get-Process, Get-Service), Task Scheduler automation |
| Lab 9 | Helpdesk Simulation | IT ticketing system, SLA management, Tier 1/2/3 escalation, user communication, password resets, VPN issues |

---

## 2. Windows Administration & PowerShell Scripting

**Cert Alignment:** Microsoft MD-102 &nbsp;|&nbsp; **Labs:** 9 · **Exercises:** 86

Deep-dive into Windows 10 administration covering the full lifecycle of a managed workstation — from deployment through security hardening — plus PowerShell scripting fundamentals.

| Lab | Title | Key Topics |
|-----|-------|------------|
| Lab 1 | Windows 10 Installation | Clean install, locale config, MDT (Microsoft Deployment Toolkit), Sysprep for imaging, setup log analysis |
| Lab 2 | Configuring Users | MMC snap-ins, local users & groups, 21 exercises: account creation/disabling/renaming/deletion, password policies, account lockout, audit policies, UAC, VPN, Remote Desktop |
| Lab 3 | Managing Data | NTFS file/folder permissions, OneDrive cloud storage, BitLocker full-disk encryption |
| Lab 4 | Managing the Windows 10 Environment | Desktop/display config, virtual memory (paging file), custom power plans, Hibernate, Windows Services lifecycle |
| Lab 5 | Configuring Network Connectivity | Static TCP/IP, DHCP configuration, wireless network properties, domain join, Active Directory integration |
| Lab 6 | Configuring Recovery | Safe Mode boot, boot logging, Windows Backup/Restore, system image creation, restore points, Recycle Bin recovery |
| Lab 7 | Managing Devices | FAT32→NTFS conversion, disk quotas, GPT vs MBR, basic→dynamic disk, simple/extended volumes, drive letter management |
| Lab 8 | Managing Security | Windows Defender advanced scan, inbound firewall rules, Application Guard (isolated browser), Credential Guard, Exploit Guard |
| Lab 9 | Working with PowerShell | DOS in PS, process management, execution policy, PSProviders, variables, comparison operators, if/switch conditionals, foreach/for loops |

---

## 3. Windows Server & Directory Administration

**Cert Alignment:** Microsoft AZ-800 &nbsp;|&nbsp; **Labs:** 12

Enterprise-level Windows Server 2019 administration covering the full server stack — from initial deployment through Active Directory, network services, remote access, containerisation, and performance monitoring.

| Lab | Title | Key Topics |
|-----|-------|------------|
| Lab 1 | Windows Server Installation & Post-Install | Windows Server 2019 clean install, post-installation software setup |
| Lab 2 | Server Manager & Command Shell | Server Manager, Windows Admin Center, PowerShell cmdlets, PSProviders, WMI queries, server admin scripts |
| Lab 3 | Hyper-V & Rapid Server Deployment | Virtual switch creation, WDS (Windows Deployment Services), OS network deployment, VM templates, VM hardware settings |
| Lab 4 | Active Directory Installation & Exploration | AD DS install, domain promotion (domain.com/DOMAINX), forest functional level, AD sites (Chicago/Paris/Toronto), distribution lists, RODC deploy/remove |
| Lab 5 | Configuring Resource Access | NFS, FSRM, DFS Namespaces & Replication, NTFS permissions (Deny overrides Allow), EFS encryption, storage quotas, file screening |
| Lab 6 | Configuring Printing | Print Server install, SamplePrinter1/2 with Type 3 drivers, AD printer objects, print queue management, troubleshooting |
| Lab 7 | Configuring & Managing Data Storage | RAID-5, Storage Spaces, iSCSI Target (iscsitarget1), Windows Server Backup, scheduled backups, file restore |
| Lab 8 | Configuring & Managing Network Services | DNS zones (zoneX.com), nslookup, WINS NetBIOS records, DHCP with name protection, DHCP failover |
| Lab 9 | Configuring & Managing Remote Access | VPN (EAP/MS-CHAPv2), RADIUS with daily logs, DirectAccess (A/AAAA records + 2 GPOs), RDS roles |
| Lab 10 | Web Services & Cloud Technologies | IIS web app, Windows Containers (iiscontainer1-3), WSL web page update, LCOW (apachecontainer3), Nano Server |
| Lab 11 | Managing & Securing Windows Networks | GPO folder redirection, AD Certificate Services, 802.1X WPA wireless, WSUS patch management, Defender firewall rules |
| Lab 12 | Monitoring & Troubleshooting | Task Manager/Resource Monitor (10 captures), performance baseline, Data Collector Sets (ETL), Event Viewer, tracert, ntbtlog.txt |

---

## 4. Network+ Labs

**Cert Alignment:** CompTIA Network+ N10-008 &nbsp;|&nbsp; **Labs:** 10 · **Source:** 131 pages

Networking fundamentals using Cisco Packet Tracer — covering the full range of network+ exam topics from topology and binary conversions through routing, switching, VLAN design, and troubleshooting.

| Lab | Title | Key Topics |
|-----|-------|------------|
| Lab 1 | Introduction to Networks | Basic topology build, end-to-end ping verification (PC↔PC, PC↔Switch) |
| Lab 2 | Conversions | Binary↔decimal↔hex IP address conversions, octet validation, invalid IP identification |
| Lab 3 | Internetworking | S1/S2 switch config, R1 router config, full mesh ping verification across all devices |
| Lab 4 | Subnetting | /19, /22, /24, /27, /28, /29, /30 calculations — network address, first/last host, broadcast, host count |
| Lab 5 | Static & Dynamic Routing | R1/R2/R3 static routes then dynamic routing, convergence verification, serial interface pings |
| Lab 6A/B | Switching, VLAN & Trunking | VLAN config, access/trunk ports, inter-VLAN routing (router-on-a-stick) — before/after ping verification |
| Lab 7 | Configuring Syslog | Syslog server setup, log capture without/with timestamps, connectivity verification |
| Lab 8 | Switchport Security | MAC address binding (max 1 device/port), rogue laptop blocked, unused port shutdown, console password |
| Lab 9 | Physical Security, Data Center & Cloud | Purging/clearing/destruction definitions, Spine/Leaf architecture, East-West traffic, cloud elasticity, SNMP, NetFlow, Syslog |
| Lab 10 | Troubleshooting | VLAN/trunking fault diagnosis — before fix: pings fail; after correcting trunk configs: all pings successful |

---

## 5. Linux Administration

**Cert Alignment:** CompTIA Linux+ / LPIC-1 &nbsp;|&nbsp; **Labs:** 12 · **Source:** 185 pages

Comprehensive Linux system administration on Fedora Linux — from installation and filesystem management through services, scripting, network configuration, and deploying key infrastructure services.

| Lab | Title | Key Topics |
|-----|-------|------------|
| Lab 2 | Linux Installation & Usage | Fedora install (LINUXrocks!), BASH basics, case-sensitivity, KDE Plasma via dnf, command substitution |
| Lab 3 | Exploring Linux Filesystems | Absolute/relative paths, cat/tac/file commands, vi editor (insert/command mode, save/quit), wildcards, grep regex |
| Lab 4 | Linux Filesystem Management | mkdir, cp -R, mv, hard/soft links (ln), chmod numeric/symbolic, chown, umask |
| Lab 5 | Linux Filesystem Administration | fdisk partitioning, mount/umount, /etc/fstab, disk quotas, fsck integrity checks, swap, LVM |
| Lab 6 | Linux Server Deployment | systemctl service lifecycle, firewalld rules, dnf/rpm package management, chrony NTP, SSH hardening |
| Lab 7 | Working with the BASH Shell | Variables, I/O redirection (>/>>/<), pipes, aliases, if/else conditionals, for/while loops in .sh scripts |
| Lab 8 | System Initialization, X Windows & Localization | GRUB parameters (single-user mode), systemd targets, X Windows, localectl, timedatectl |
| Lab 9 | Managing Linux Processes | ps -el, top, kill SIGTERM, cron job (/bin/false at 30 20 * * *), nice/renice priority |
| Lab 10 | Common Administrative Tasks | useradd (bozo, /bin/bash), chage -W 5, account lock/unlock at tty6, chown, logrotate config |
| Lab 11 | Compression, Backup & Software | ncompress, tar -zcvf, gzip/bzip2/xz comparison, rpm queries, dnf group installs |
| Lab 12 | Network Configuration | ifdown/ifup eth0, networkctl, ip addr/ifconfig, /etc/resolv.conf, SSH localhost, ss -t, X11 forwarding |
| Lab 13 | Network Services & Cloud Technologies | DHCP (dhcpd), Apache httpd (marketingapp), Samba (smb.conf/testparm/smbclient), SFTP, Postfix email, PostgreSQL (sales DB/customer table/bob privileges) |

---

## 6. Cisco Technologies (CCNA)

**Cert Alignment:** Cisco CCNA 200-301 &nbsp;|&nbsp; **Labs:** 14 · **Hardware:** Physical Cisco Catalyst 1000 switches & 4221 routers

The most hardware-intensive course — all labs completed on physical Cisco equipment. Covers the full CCNA curriculum from basic configuration through advanced routing protocols, security, and redundancy.

| Lab | Title | Key Topics |
|-----|-------|------------|
| Lab 1 | Initial Configuration — Switches & Router | Hostname/passwords/MOTD/MOTD, S1 management IP, R1 G0/0/1 LAN + S0/1/0 WAN serial, SSH/console/VTY |
| Lab 2 | DHCP Configuration (Local & Remote) | DHCP pools on R1/R2/R3, full ping verification, ip helper-address for remote DHCP relay across WAN |
| Lab 3 | Subnetting | 3 scenarios: /24→/26 (3 subnets), /24→/27 (8 subnets), /16→/20 (15 subnets). Subnet tables completed |
| Lab 4 | Subnetting Implementation | VLSM design from 172.21.55.64/27, physical config on 3 routers + 3 switches, full mesh connectivity |
| Lab 5 | Dynamic Routing Using OSPF | OSPFv2 process config, network statements, neighbour adjacency (show ip ospf neighbor), routing table verification |
| Lab 6 | OSPFv2 Routing & Verification | 4-router topology, complete ping matrix, show ip route/ospf neighbor/ospf/interface brief on all routers |
| Lab 7 | OSPFv3 Routing & Verification | IPv6 OSPFv3 on 4 routers, show ipv6 route/ospf neighbor/protocols/ospf interfaces |
| Lab 8 | STP & EtherChannel | Root bridge elected (S3, lowest MAC 0005.5E79.4C37), root ports, S2 f0/2 blocked. LACP EtherChannel on all 3 switches |
| Lab 9 | Access Control Lists | Standard/extended ACLs on R1/R3 — S1→File Server: ✓ permitted, S1→Web Server: ✗ denied, S2→File Server: ✗ denied |
| Lab 10 | Configuring NAT | Static NAT (PC-A↔public IP), dynamic NAT (pool-based), show ip nat translations/statistics |
| Lab 11 | Configuring PAT | NAT pool overload, PAT single IP, clear ip nat trans *, port multiplexing verification |
| Lab 12 | Configuring RADIUS | Local AAA (aaa new-model), Telnet fix (transport input telnet), hashed secrets, RADIUS centralized auth |
| Lab 13 | Configuration of HSRP | OSPF + HSRP group (BR_R1 Active, BR_R2 Standby), failover test (shutdown G0/0 → auto failover), Hello packets in simulation mode |
| Lab 14 | Configuring GRE Tunnels | interface tunnel 0, tunnel source/destination, OSPF over tunnel, traceroute confirms GRE path end-to-end |

---

## 7. Security+ Labs

**Cert Alignment:** CompTIA Security+ SY0-701 &nbsp;|&nbsp; **Lab Sections:** 7 · **Cloud Platform:** AWS

Offensive and defensive security labs covering packet crafting, cloud security assessment, identity management, web application exploitation, network intrusion detection, and risk management frameworks.

| Lab | Title | Key Topics |
|-----|-------|------------|
| Lab 6* | Packet Crafting & Password Attacks | Scapy: ICMP crafting, TCP packets, SYN flood DoS. Mimikatz: sekurlsa::logonpasswords hash extraction. John the Ripper: dictionary crack |
| Lab 7 | Cloud Security | ScoutSuite: compliance scanning (HIPAA/PCI-DSS/GDPR), public S3 buckets, overprivileged IAM. Pacu: AWS red team framework, misconfigured resources, exposed keys |
| Lab 8 | Identity & Access Management Security | OAuth/HTTPS vulnerability (HTTP between servers), Facebook Login risk analysis, emergency privilege escalation plan, privilege creep audit → RBAC + least privilege |
| Lab 9 | Software Development Security & SIEM | OWASP SQL injection — 10 remediation steps (prepared statements, WAF, input validation). WebGoat exploits. AlienVault/Security Onion SIEM deployed in VirtualBox |
| Lab 10 | Analyzing Indicators of Compromise | Nmap against Metasploitable: open ports/services. Wireshark: TCP handshake (SYN/SYN-ACK/ACK/RST) for port 22. HTTP traffic capture. SSH exposure remediation |
| Lab 11 | NIDS — Snort (Three Modes) | Snort sniffer mode (snort -vd: L3/4 headers; snort -ve: link-layer). Packet logger mode: log file generated, opened in Wireshark, ping traffic analysed |
| Lab 12 | Risk Management & Compliance | Risk strategies: avoidance/transference/mitigation/acceptance with examples. NIST CSF PR.AC-1 through PR.AC-5. Policy hierarchy: Policy → Standard → Guideline → Procedure |

---

## 8. Ethical Hacking

**Cert Alignment:** CEH / CompTIA PenTest+ &nbsp;|&nbsp; **Labs:** 12

Full penetration testing lifecycle from reconnaissance through exploitation, post-exploitation, and hardening — covering the complete attacker and defender mindset.

| Lab | Title | Key Topics |
|-----|-------|------------|
| Lab 1 | Hacker Mindset & Cyber Kill Chain | Physical security analysis (POS/CCTV/EAS weaknesses). SolarWinds 2020 kill chain: Recon → Weaponization (SUNBURST) → Delivery → Exploitation → C2 → Exfiltration |
| Lab 2 | Planning & Scoping | GDPR 7 principles, white/grey/black-box assessment types, legal agreements (SLA/NDA/MSA/SOW), mobile banking app scope definition |
| Lab 3 | Information Gathering | dig +dnssec (ZSK/KSK keys), WHOIS (Cloudflare), traceroute (Akamai/Ottawa), theHarvester, Shodan (29,905 Facebook results), Censys, Nmap (-sV/-sU/-p 1-65535) |
| Lab 4 | Vulnerability Analysis | GVM/OpenVAS: 10 vulns on Win Server 2019 (CVSS 10.0), CVE-2022-26927 RCE. Nessus install + scan. MCDS stealthy scanning plan (slow/spoofed) |
| Lab 5 | Interpreting Scans & Pen Test Planning | CVSS vector analysis (SSL cert higher severity due to A:H). OSINT on mcdsllc.com. 3 exploitation scenarios: IP disclosure, SQL injection, POODLE SSLv3 |
| Lab 6 | Exploitation — SQL Injection & PowerShell | DVWA/MariaDB: users table enumeration, OR-based bypass. PowerShell: DownloadString remote execution, script7.ps1 ping commands, remote shutdown |
| Lab 7 | Hashes, Brute Force & Wireless | Hash capture in VirtualBox. Hydra brute force with rockyou.txt (successful crack). WPA2 cracking, deauthentication attacks with Wifite |
| Lab 8 | Social Engineering Tools | SET malicious USB (payload.exe). BeEF: browser hook established, real-time dashboard control. Facebook clone page via SET: credentials captured |
| Lab 9 | Exploiting Application Vulnerabilities | ZAP Proxy: live traffic interception. Stored XSS: script injected in source, executed on page load. IDOR: ?id=501 through ?id=505 — sequential user records accessed |
| Lab 10 | Exploiting Host Vulnerabilities | Meterpreter on Metasploitable 3: getuid + hashdump. Hashcat + rockyou.txt: hashes cracked. Reverse shell via LHOST. Bind vs reverse shell comparison |
| Lab 11 | System Hardening | AD DS join (domain407.com, client OLADAPOAFOLABI-CLIENT). OU structure: TorontoTWS with sub-OUs. Delegation: Account Operators/Server Operators. Global/Domain Local/Universal groups |
| Lab 12 | Social Engineering in Action | Sneakers (1992): 8 SE techniques identified. Kevin Mitnick: pretexting/tailgating/shoulder surfing analysis. Real-world password disclosure + 6 preventive controls |

---

## 9. IT Security Forensics

**Cert Alignment:** EC-Council CHFI &nbsp;|&nbsp; **Labs:** 10

Complete digital forensics investigation lifecycle — from evidence acquisition and crime scene processing through advanced analysis, steganography detection, email forensics, and mobile tool comparison.

| Lab | Title | Key Topics |
|-----|-------|------------|
| Lab 1 | Investigation Using Autopsy | Workplace misconduct case — George's disk. Findings: Amelia Phillips' laptop, files accessed at 14:50 EST, domain records, client PII spreadsheet. AUP/Data Protection policies identified |
| Lab 2 | The Investigator's Office & Laboratory | ABC Corp forensics policy (5-step process, GDPR/NIST SP 800-86/ISO 27037). CHFI certification research (EC-Council, ANAB/DoD accredited). Acme Corp DRP (daily/weekly/monthly backups) |
| Lab 3 | Data Acquisition | Mini-WinFE forensic boot environment. Linux (dd/rsync) vs Windows (FTK Imager/EnCase) acquisition comparison table. Hands-on: USB disk image with FTK Imager |
| Lab 4 | Processing Crime & Incident Scenes | OSForensics metadata viewing. Hash verification: Original MD5 8e85440c... → After editing: 0f74de60... (complete hash change proves tamper detection) |
| Lab 5 | Working with Windows & CLI Systems | WinHex: unique hex signatures per file type, detects alterations. Registry viewer: hive exploration. OSForensics: extracted Wi-Fi passwords + Chrome browser credentials |
| Lab 6 | Current Digital Forensic Tools | EnCase/FTK/Nuix/EasyRecovery feature matrix. Mac hex editors: 0xED, Hex Fiend (118GB). Linux: HxD, Okteta. ISO 17025:2017 validation procedure |
| Lab 7A/B | Linux & Macintosh File Systems | Cellebrite UFED ($6-15K) vs Magnet AXIOM ($3-6K, recommended) vs Oxygen ($2-4K). Free tool comparison: Autopsy vs OSForensics vs FTK Imager |
| Lab 8 | Digital Forensics Analysis & Validation | File carving (C08frag with 'jfif', C08carve with 'zzzz'). Image format conversions (BMP/JPG/GIF size/quality analysis). LSB steganography detected: 10 byte-level ±1 deviations in mission-steg.bmp |
| Lab 9 | VM Forensics, Live Acquisitions & Network Forensics | USB forensic lab design (VirtualBox/VMware/Hyper-V + 10 forensic tools). VM security best practices: 10-item checklist for secure software distribution |
| Lab 10 | Email & Social Media Investigations | Aid4Mail: Eric Saibi .pst → CSV export → Enron scandal emails + PII found. Social media forensic plan: FTK Imager image → Autopsy metadata/IP/cookies analysis |

---

## 🛠️ Tools & Technologies

### Networking & Infrastructure
`Cisco IOS` · `Cisco Catalyst 1000` · `Cisco 4221` · `Cisco Packet Tracer` · `OSPFv2/v3` · `DHCP` · `DNS` · `WINS` · `Active Directory` · `Wireshark` · `Nmap` · `VPN/GRE` · `HSRP` · `STP` · `LACP EtherChannel` · `NAT/PAT`

### Security & Offensive Tools
`Kali Linux` · `Metasploit` · `Meterpreter` · `Mimikatz` · `Hashcat` · `John the Ripper` · `Hydra` · `Scapy` · `BeEF` · `SET (Social Engineer Toolkit)` · `Snort` · `OWASP ZAP` · `GVM/OpenVAS` · `Nessus`

### Cloud & Virtualisation
`ScoutSuite` · `Pacu (AWS)` · `Hyper-V` · `VirtualBox` · `VMware` · `Docker` · `WSL` · `Windows Containers` · `Nano Server` · `LCOW` · `IIS`

### Digital Forensics
`Autopsy` · `FTK Imager` · `OSForensics` · `WinHex` · `EnCase` · `Magnet AXIOM` · `Cellebrite UFED` · `Aid4Mail` · `Volatility` · `Mini-WinFE`

### Systems & Scripting
`Windows Server 2019` · `Windows 10/11` · `Fedora Linux` · `PowerShell` · `BASH` · `Apache httpd` · `Samba` · `Postfix` · `PostgreSQL`

---

## 📊 Portfolio Stats

| Metric | Count |
|--------|-------|
| Courses completed | 9 |
| Total labs | 95+ |
| Total exercises | 400+ |
| Physical Cisco labs | 14 (Catalyst 1000 + 4221 routers) |
| Pages of lab content processed | 316+ (Network+ 131 + Linux 185) |
| Forensic investigations | 10 |
| Penetration testing labs | 12 |

---

## 📁 Repository Structure

```
cybersecurity-lab-portfolio/
├── index.html                              ← Portfolio landing page (GitHub Pages)
├── README.md                               ← This file — full course & lab overview
├── Windows_Admin_PowerShell_README.md      ← Course 2
├── Windows_Server_Directory_Admin_README.md ← Course 3
├── Network_Plus_Labs_README.md             ← Course 4
├── Linux_Administration_Labs_README.md     ← Course 5
├── Cisco_CCNA_Labs_README.md               ← Course 6
├── Security_Plus_Labs_README.md            ← Course 7
├── Ethical_Hacking_Labs_README.md          ← Course 8
└── IT_Security_Forensics_README.md         ← Course 9
```

---

*Portfolio maintained by [Your Name] · [LinkedIn] · [Your Email]*
