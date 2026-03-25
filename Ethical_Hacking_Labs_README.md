# 🎯 Ethical Hacking — Lab Portfolio

Hands-on labs covering the full **penetration testing lifecycle** — from reconnaissance through exploitation, post-exploitation, hardening, and social engineering — using Kali Linux, Metasploit, VirtualBox, and industry-standard offensive security tools.

---

## 📋 Table of Contents

| # | Lab | Topics |
|---|-----|--------|
| 1 | Hacker Mindset and Cyber Kill Chain | Kill chain analysis, SolarWinds case study |
| 2 | Planning and Scoping | GDPR, assessment types, legal agreements |
| 3 | Information Gathering | OSINT, dig, WHOIS, theHarvester, Shodan, Nmap |
| 4 | Vulnerability Analysis | GVM/OpenVAS, Nessus, CVE identification |
| 5 | Interpreting Vulnerability Scans & Pen Test Planning | CVSS analysis, OSINT recon, exploitation planning |
| 6 | Exploitation — SQL Injection & PowerShell | DVWA, SQL injection, PowerShell exploitation |
| 7 | Capturing Hashes, Brute Forcing & Wireless Testing | Hash capture, Hydra, WPA2 cracking |
| 8 | Social Engineering Tools | SET, BeEF, phishing, clone pages |
| 9 | Exploiting Application Vulnerabilities | ZAP proxy, XSS, IDOR |
| 10 | Exploiting Host Vulnerabilities | SAM dump, Hashcat, Meterpreter shells |
| 11 | System Hardening | Active Directory, OUs, RBAC, delegation |
| 12 | Social Engineering in Action | Movie SE analysis, real-world password disclosure |

---

## Lab 1: Hacker Mindset and Cyber Kill Chain

### Physical Security Analysis
| Control | Weakness |
|---------|----------|
| Security guard patrols | Can be distracted via social engineering |
| CCTV cameras | Often unmonitored, exploitable systems |
| EAS anti-theft tags | Only on expensive items, can be deactivated |
| POS registers | Self-checkout exploits, POS vulnerabilities |

### SolarWinds Kill Chain Analysis
| Phase | Application |
|-------|-------------|
| Reconnaissance | OSINT/SE to gather SolarWinds system info |
| Weaponization | SUNBURST backdoor injected into update packages |
| Delivery | Trojanized updates with valid signatures to 18,000+ customers |
| Exploitation | Backdoor activated upon installation |
| Installation | Additional malware, lateral movement |
| C2 | Covert channels for remote control |
| Actions | Sensitive data theft from government/enterprise |

**Key Concepts:** Kill chain · Supply chain attacks · SUNBURST · APT tactics

---

## Lab 2: Planning and Scoping

**GDPR 7 Principles:** Lawful/fair/transparent · Purpose limitation · Data minimisation · Accuracy · Storage limitation · Integrity/confidentiality · Accountability

**Assessment Types:** White-box (full knowledge) · Grey-box (partial) · Black-box (simulates real attack)

**Legal Agreements:** SLA · NDA · MSA · SOW

**Scope (Mobile Banking App):** In-scope: mobile app, API gateway, auth server, transaction server, database. Out-of-scope: core banking systems, unrelated apps.

---

## Lab 3: Information Gathering

- `dig a www.afrinic.net` → IP: 196.216.2.6 · `dig +dnssec` → 2 ZSK + 1 KSK keys
- `dig +trace` — full DNS resolution path
- WHOIS: hosting by **Cloudflare Inc.** (101 Townsend St, SF, CA)
- Traceroute: company hosted by **Akamai Technologies**, Ottawa, ON, Canada
- Shodan: Facebook search → 29,905 results · Censys provides deeper vulnerability detail
- Nmap: basic scan · full port scan (`-p 1-65535`) · service detection (`-sV`) · UDP scan (`-sU`)

**Tools:** `dig` · `whois` · `traceroute` · `theHarvester` · Shodan · Censys · Nmap

---

## Lab 4: Vulnerability Analysis

**GVM/OpenVAS Results:**
| Target | Severity | Top CVEs |
|--------|----------|---------|
| Windows Server 2019 | 10.0 High | CVE-2022-26923, CVE-2022-26927 |
| Windows Enterprise 11 | 10.0 High | CVE-2022-26925, CVE-2022-26928 |

**Nessus:** Installed and executed vulnerability scan.

**Scanning Plan (MCDS Networks):** Stealthy slow scans from multiple locations with spoofed IPs.

**Tools:** GVM/OpenVAS · Nessus · Kali Linux

---

## Lab 5: Interpreting Vulnerability Scans & Pen Test Planning

**CVSS Analysis:** SSL Certificate vulnerability scored higher due to greater availability impact (AV:N/AC:L/PR:N impacts C:L/I:L/A:H).

**OSINT on MCDS LLC:**
- Domain: `mcdsllc.com` · IP: `13.248.243.5` · 4 employees · Remote VPN access
- Tech: Apache, Windows 10, Office 365 · Social: Instagram + Facebook

**Exploitation Scenarios:**
1. HTTP Header Internal IP Disclosure — map internal network, lateral movement
2. CGI Blind Time-Based SQL Injection — extract credentials, escalate DB privileges
3. POODLE (SSLv3) — session cookie decryption, session hijacking

---

## Lab 6: Exploitation — SQL Injection & PowerShell

**SQL Injection (DVWA/MariaDB):** Enumerated users table · Queried user records · `OR` operator extracted all users

**PowerShell Exploitation:**
- `DownloadString` to execute remote PS content
- `script3.ps1` and `script7.ps1` executed remotely
- Remote shutdown command via PowerShell

**Also:** Metasploitable scanning, meterpreter shell, CodeExecution module

**Tools:** WampServer · DVWA · MariaDB · PowerShell · Metasploit

---

## Lab 7: Capturing Hashes, Brute Forcing & Wireless Testing

- Captured authentication hashes in VirtualBox environment
- **Hydra** brute force with `rockyou.txt.gz` — crack successful
- `-t` flag adjusts thread count; custom passwords added to wordlist

**Tools:** Hydra · Wireshark · Wifite · `rockyou.txt` · Kali Linux

**Key Concepts:** Hash capture · NTLM · Brute force · WPA2 cracking · Deauthentication attacks

---

## Lab 8: Social Engineering Tools

- **SET Malicious USB:** Created `payload.exe` — USB infection vector
- **BeEF:** Browser hook established — real-time browser control via dashboard
- **Phishing tests:** GreatHorn · SonicWall · OpenDNS platforms
- **SET Facebook clone:** Phishing page captured credentials · Phishing email sent

**Tools:** SET · BeEF · GreatHorn · SonicWall · VMware · Kali Linux

**Key Concepts:** Credential harvesting · Clone phishing · USB attack vectors · Browser hooking

---

## Lab 9: Exploiting Application Vulnerabilities

- **ZAP Proxy:** Browser traffic intercepted — requests viewed and modified
- **XSS:** Injected malicious script into source code — executed in browser after refresh (stored XSS)
- **IDOR:** URL manipulation `?id=501` through `?id=505` — accessed different user records without authorization

**Tools:** OWASP ZAP · PHP · MySQL · Kali Linux

**Key Concepts:** ZAP proxy · Stored XSS · IDOR · Input validation · WAF

---

## Lab 10: Exploiting Host Vulnerabilities

- Meterpreter session on Metasploitable 3 — `getuid` confirmed context
- `hashdump` — Windows password hashes extracted
- **Hashcat** with `rockyou.txt` — hashes cracked (including complex personal password after adding to wordlist)
- Reverse shell configured with `LHOST` — Meterpreter session established

**Tools:** Metasploit · Meterpreter · Hashcat · rockyou.txt · Metasploitable 3

**Key Concepts:** SAM database · Hash dumping · Hashcat modes · Reverse vs bind shell

---

## Lab 11: System Hardening

**AD Domain Controller (Windows Server 2019):**
- Client renamed to `OLADAPOAFOLABI-CLIENT` — joined `domain407.com` ✓
- Computer object appeared in ADUC with full OS info

**OU Structure (TorontoTWS):**
- OUs and sub-OUs created · Bursar OU deleted · Computer moved to Students Desktop
- `Account Operators` delegated to Users OU · `Server Operators` to Servers OU
- Waterloo OU managed by Administrator

**Groups created:** Global (IT) · Domain Local (Students) · Universal (HR)

**Key Concepts:** AD DS · Domain join · OUs · Delegation · RBAC · Group types · Least privilege

---

## Lab 12: Social Engineering in Action

### Sneakers (1992) — SE Techniques
Tailgating · Phishing · Reverse SE · Dumpster diving · Impersonation · Shoulder surfing · Pretexting · Whaling (NSA executive targeted)

### Kevin Mitnick (Operation Takedown)
- Pretexting/impersonation to extract system info
- Tailgating + shoulder surfing on university campus
- Baiting with staged emergencies

### Preventive Controls
Security awareness training · Strong password policies · MFA/2FA · Email filtering · Identity verification · Incident response plan

**Key Concepts:** Tailgating · Phishing · Pretexting · Whaling · Human vulnerability · MFA

---

## 🛠️ Tools & Technologies Used

`Kali Linux` · `Metasploit` · `Meterpreter` · `Nmap` · `Nessus` · `GVM/OpenVAS` · `Hydra` · `Hashcat` · `John the Ripper` · `Wireshark` · `OWASP ZAP` · `BeEF` · `SET` · `Shodan` · `Censys` · `theHarvester` · `Wifite` · `WampServer` · `DVWA` · `MariaDB` · `PowerShell` · `VirtualBox` · `VMware` · `Windows Server 2019` · `Active Directory` · `dig` · `whois` · `traceroute` · `rockyou.txt`

---

*Portfolio maintained by [Your Name] · [LinkedIn] · [Your Email]*
