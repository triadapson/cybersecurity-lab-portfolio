# 🖥️ Computer & Networking Fundamentals (A+) — Lab Portfolio

A collection of hands-on labs completed as part of a **CompTIA A+ aligned** course in Computer and Networking Fundamentals. These labs cover hardware, networking, operating systems, security, and scripting — building a strong foundation in IT support and cybersecurity.

---

## 📋 Table of Contents

| # | Lab | Topics |
|---|-----|--------|
| 1 | [Hardware & Components](#lab-1-hardware--components) | PC parts, peripherals, connectors |
| 2 | [Network Topology](#lab-2-network-topology) | LAN/WAN, topology types, cabling |
| 3 | [TCP/IP and Networking Fundamentals](#lab-3-tcpip-and-networking-fundamentals) | IP addressing, subnetting, protocols |
| 4 | [Operating System Fundamentals](#lab-4-operating-system-fundamentals) | Windows, Linux, macOS basics |
| 5 | [Security Concepts](#lab-5-security-concepts) | Threats, malware, authentication, encryption |
| 6 | [Troubleshooting Methodology](#lab-6-troubleshooting-methodology) | CompTIA 6-step troubleshooting model |
| 7 | [IT Policies and Procedures](#lab-7-it-policies-and-procedures) | AUP, change management, documentation |
| 8 | [Scripting and Automation Basics](#lab-8-scripting-and-automation-basics) | Batch files, PowerShell basics, automation |
| 9 | [Helpdesk Simulation](#lab-9-helpdesk-simulation) | Ticketing system, communication, escalation |

---

## Lab 1: Hardware & Components

**Objective:** Identify and describe the function of key PC components, peripherals, and connectors.

**Activities:**
- Identified motherboard components: CPU socket, RAM slots, PCIe slots, CMOS battery, chipset, SATA ports
- Distinguished RAM types: DDR3, DDR4, DDR5 — DIMM vs SO-DIMM form factors
- Identified storage: HDD, SSD (SATA, NVMe M.2), optical drives
- Identified ports: USB-A, USB-C, HDMI, DisplayPort, VGA, RJ-45, audio jacks
- Identified PSU connectors: 24-pin ATX, 8-pin CPU, SATA power, Molex
- Identified expansion cards: GPU, NIC, sound card, RAID controller

**Key Concepts:** Motherboard form factors · CPU cooling · Storage interfaces (SATA, NVMe) · Power delivery

---

## Lab 2: Network Topology

**Objective:** Understand network topologies and cable types in LAN/WAN environments.

**Activities:**
- Identified topology types: Bus, Star, Ring, Mesh, Hybrid — advantages and disadvantages
- Distinguished LAN vs WAN vs MAN
- Identified cable types: Cat5e, Cat6, Cat6a, fibre optic (single-mode, multi-mode)
- Identified connectors: RJ-45, RJ-11, SC, LC, ST
- Explained wireless standards: 802.11a/b/g/n/ac/ax (Wi-Fi 6)
- Identified network devices: hub, switch, router, access point, modem, firewall

**Key Concepts:** Star topology · Cable categories and speeds · 2.4GHz vs 5GHz · Network device roles

---

## Lab 3: TCP/IP and Networking Fundamentals

**Objective:** Apply TCP/IP concepts including IP addressing, subnetting, and common protocols.

**Activities:**
- Identified IPv4 address classes (A, B, C) and private ranges
- Performed subnetting calculations (subnet mask, network address, broadcast, valid hosts)
- Distinguished IPv4 vs IPv6 addressing
- Identified common protocols and ports:

| Protocol | Port | Function |
|----------|------|----------|
| HTTP | 80 | Web browsing |
| HTTPS | 443 | Secure web |
| FTP | 20/21 | File transfer |
| SSH | 22 | Secure remote access |
| DNS | 53 | Name resolution |
| DHCP | 67/68 | IP assignment |
| SMTP | 25 | Email sending |
| RDP | 3389 | Remote desktop |

- Used `ipconfig`, `ping`, `tracert`, `nslookup` on Windows
- Explained TCP vs UDP (connection-oriented vs connectionless)
- Described OSI model (7 layers) and TCP/IP model (4 layers)

**Tools:** Windows Command Prompt · `ipconfig` · `ping` · `tracert` · `nslookup`

**Key Concepts:** IP addressing · Subnetting · Common ports · OSI layers · TCP vs UDP

---

## Lab 4: Operating System Fundamentals

**Objective:** Navigate and perform basic administration in Windows, Linux, and macOS.

**Windows Activities:**
- File system navigation with File Explorer and Command Prompt
- Commands: `cd`, `dir`, `mkdir`, `del`, `copy`, `move`, `cls`
- System Properties, Device Manager, Task Manager
- Tools: `msconfig`, `regedit`, `services.msc`

**Linux Activities:**
- Commands: `ls`, `cd`, `pwd`, `cp`, `mv`, `rm`, `mkdir`, `cat`, `grep`
- Linux directory structure: `/home`, `/etc`, `/var`, `/bin`
- Processes with `ps` and `top`

**macOS Activities:**
- Finder and Terminal navigation
- Activity Monitor, Disk Utility, System Preferences

**Key Concepts:** CLI basics · File system navigation · Process management · OS tools

---

## Lab 5: Security Concepts

**Objective:** Understand security threats, authentication methods, and encryption.

**Activities:**
- Malware types: virus, worm, trojan, ransomware, spyware, adware, rootkit, keylogger
- Social engineering: phishing, spear phishing, vishing, smishing, tailgating, pretexting
- Authentication factors:
  - Something you know (password, PIN)
  - Something you have (smart card, token)
  - Something you are (fingerprint, face)
- MFA (Multi-Factor Authentication) and why it matters
- Encryption: symmetric vs asymmetric
- Protocols: HTTPS/TLS, WPA2/WPA3, VPN
- CIA Triad: Confidentiality, Integrity, Availability
- Physical security: locks, cameras, badge access, mantraps

**Key Concepts:** Malware types · Social engineering · MFA · CIA triad · Encryption

---

## Lab 6: Troubleshooting Methodology

**Objective:** Apply the CompTIA 6-step troubleshooting methodology.

| Step | Action |
|------|--------|
| 1 | Identify the problem — gather info, question the user |
| 2 | Establish a theory of probable cause |
| 3 | Test the theory to determine the cause |
| 4 | Establish a plan and implement the solution |
| 5 | Verify full system functionality and add preventive measures |
| 6 | Document findings, actions, and outcomes |

**Scenarios:**
- Computer won’t boot: POST errors, RAM seating, power supply
- No internet: `ipconfig /release`, `ipconfig /renew`, DNS flush
- Slow computer: Task Manager, startup programs, disk cleanup
- Printer not printing: print queue, driver reinstall
- No display: cable, GPU seating, monitor input

**Key Concepts:** Systematic troubleshooting · Root cause analysis · Documentation

---

## Lab 7: IT Policies and Procedures

**Objective:** Understand IT policies including AUP, change management, and data handling.

**Activities:**
- Analysed an Acceptable Use Policy (AUP) — permitted/prohibited use, monitoring, consequences
- Change management: request → approval → testing → implementation → review
- Data classification: public, internal, confidential, restricted
- BYOD policies and risks
- Incident response: identify → contain → eradicate → recover → lessons learned
- Compliance frameworks: GDPR, HIPAA, PCI-DSS

**Key Concepts:** AUP · Change management · Data classification · Incident response · Compliance

---

## Lab 8: Scripting and Automation Basics

**Objective:** Create basic automation scripts using Batch files and introductory PowerShell.

**Batch Files (.bat):**
- Automated folder creation and file backup
- Used variables, `echo`, `pause`, `if`, `for` constructs
- Scheduled with Windows Task Scheduler

**PowerShell Basics:**
- `Get-Help` · `Get-Process` · `Get-Service` · `Get-EventLog`
- `Set-ExecutionPolicy` to enable script execution
- Created a `.ps1` script to display system info

**Tools:** Notepad · Command Prompt · PowerShell · Task Scheduler

**Key Concepts:** Batch scripting · PowerShell cmdlets · Execution policy · Task automation

---

## Lab 9: Helpdesk Simulation

**Objective:** Simulate helpdesk scenarios with ticket management, user communication, and escalation.

**Activities:**
- Logged and managed tickets in a simulated ticketing system
- Professional communication: clear, empathetic, non-technical language
- Resolved tickets for: password resets, email config, printer issues, VPN problems
- Documented resolution steps
- Escalation decisions: Tier 1 vs Tier 2/3
- SLA (Service Level Agreement) response and resolution time requirements

**Key Concepts:** IT ticketing · SLA management · Tier 1/2/3 support · Escalation procedures

---

## 🛠️ Tools & Technologies Used

`Windows 10/11` · `Command Prompt` · `PowerShell` · `Task Manager` · `Device Manager` · `Event Viewer` · `ipconfig` · `ping` · `tracert` · `nslookup` · `File Explorer` · `Task Scheduler` · `Linux CLI` · `macOS Terminal` · `IT Ticketing System`

---

## 📚 Course Context

These labs are part of a **Computer & Networking Fundamentals** course aligned with **CompTIA A+** (220-1101 and 220-1102) exam objectives, covering hardware, networking, operating systems, security, and operational procedures for entry-level IT support.

---

*Portfolio maintained by [Your Name] · [LinkedIn] · [Your Email]*
