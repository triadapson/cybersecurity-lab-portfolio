# 🔐 Security+ Labs — Portfolio

Hands-on labs covering **CompTIA Security+** concepts including offensive tools, cloud security, identity management, application security, network scanning, intrusion detection, and risk management — using Kali Linux, VirtualBox, and industry-standard security tools.

All screenshots to Labs can be found here : https://docs.google.com/document/d/1yvZiNqmRmdoeEZWrFD_dYUG4iAeJF-5E/edit?usp=drive_link&ouid=102757233326623178029&rtpof=true&sd=true
---

## 📋 Table of Contents

| # | Lab | Topics |
|---|-----|--------|
| 6* | Packet Crafting & Password Attacks | Scapy, SYN flood, Mimikatz, John the Ripper |
| 7 | Cloud Security | ScoutSuite, Pacu AWS exploitation framework |
| 8 | Identity and Access Management Security | OAuth, privilege creep, RBAC, AAA, MFA |
| 9 | Software & Hardware Development Security and SIEM | OWASP, SQL injection, WebGoat, SIEM |
| 10 | Analyzing Indicators of Compromise | Nmap, Wireshark, Metasploitable, port analysis |
| 11 | NIDS — Snort with Three Modes | Snort sniffer mode, packet logger, Wireshark |
| 12 | Risk Management Strategies, Policy & Compliance | Risk strategies, NIST CSF, policy hierarchy |

---

## Lab 6 (Continuation): Packet Crafting & Password Attacks

### Activity 3 — Scapy Packet Crafting
- Crafted ICMP message — captured in Wireshark
- Sent TCP packet with `sr1(ip/tcp)` and reviewed response
- Executed **SYN flood attack** via Scapy — demonstrated DoS technique

**Tools:** Scapy · Wireshark · Kali Linux

### Activity 4 — Mimikatz & John the Ripper
- Launched Mimikatz on Windows VM
- Extracted Windows credential hashes (`sekurlsa::logonpasswords`)
- Cracked hashes with John the Ripper (dictionary attack)

**Tools:** Mimikatz · crunch · John the Ripper · Kali Linux

**Key Concepts:** Packet crafting · SYN flood · NTLM hash dumping · Dictionary attacks

---

## Lab 7: Cloud Security

### ScoutSuite — Cloud Assessment
- Installed ScoutSuite in Python virtual environment
- Scans for: compliance (HIPAA, PCI-DSS, GDPR), public S3 buckets, overprivileged IAM roles, dangerous security group rules

### Pacu — AWS Exploitation Framework
- Installed and launched Pacu offensive AWS framework
- Capabilities: misconfigured resources, vulnerable access keys, open ports, cloud storage attacks

**Case Study:** Simulated e-commerce assessment — found unprotected data, exposed keys, open port 22.

**Reflection:** ScoutSuite = defensive CSPM; Pacu = offensive red team — together provide comprehensive cloud coverage.

**Key Concepts:** CSPM · AWS IAM misconfigurations · S3 security · Compliance scanning

---

## Lab 8: Identity and Access Management Security

### Federated Security Scenarios
- Identified HTTP (not HTTPS) between OAuth servers — recommended HTTPS + tested OAuth libraries
- Facebook Login risk analysis: reduced user management burden, but cascading breach risk
- Emergency privilege escalation: local accounts with MFA and RBAC
- Privilege creep: permission audit, RBAC with least-privilege, access request workflow

**Key Concepts:** OAuth 2.0 · Federated identity · Privilege creep · RBAC · Least privilege · MFA · AAA · CIA triad

---

## Lab 9: Software & Hardware Development Security and SIEM

### OWASP SQL Injection Remediation
1. Input validation · 2. Prepared statements · 3. Escape special characters · 4. Limit DB permissions · 5. Regular updates · 6. Code review · 7. WAF · 8. Secure error handling · 9. Secure coding · 10. Security audits

### WebGoat & SIEM
- Practised web exploits in WebGoat intentionally vulnerable app
- Deployed AlienVault/Security Onion SIEM in VirtualBox — analysed real-time alerts

**Tools:** OWASP ZAP · WebGoat · AlienVault/Security Onion · VirtualBox

**Key Concepts:** SQL injection · OWASP Top 10 · WAF · SIEM · Event correlation

---

## Lab 10: Analyzing Indicators of Compromise

### Network Scanning (VirtualBox)
- Wireshark capture on `eth0`
- Nmap against Metasploitable — identified open ports/services
- TCP handshake for port 22 (SYN/SYN-ACK/ACK/RST) — open port confirmed
- HTTP traffic captured visiting Metasploitable web server (port 80)

### Security Incident: Port 22 (SSH) Open
**Impacts:** Unauthorized access · Malware upload · Data theft · System takeover

**Remediation:** Disable SSH from internet · SSH keys · Trusted IP restriction · MFA · VPN alternative

**Tools:** Nmap · Wireshark · Kali Linux · Metasploitable

---

## Lab 11: NIDS — Snort with Three Modes

### Sniffer Mode
- `sudo snort -vd` — Layer 3/4 headers + upper-layer data
- `sudo snort -ve` — link-layer headers included
- Captured pings from Windows 10 machine and Ubuntu loopback

### Packet Logger Mode
- Configured Snort to generate log file during live traffic
- Opened log in Wireshark — analysed captured ping traffic

**Tools:** Snort · Wireshark · Ubuntu

**Key Concepts:** NIDS configuration · Snort modes · Layer 3/4 header analysis · Intrusion detection

---

## Lab 12: Risk Management Strategies, Policy & Compliance

### Risk Response Strategies
| Strategy | Definition | Example |
|----------|------------|---------|
| **Avoidance** | Eliminate the risk activity | Avoid insecure supplier |
| **Transference** | Shift risk to another party | Purchase cyber insurance |
| **Mitigation** | Reduce likelihood/impact | Security awareness training |
| **Acceptance** | Acknowledge and accept | Continue outdated software when upgrade cost > risk |

### NIST CSF — PR.AC Controls
| Control | Implementation |
|---------|---------------|
| PR.AC-1 | Identity & access management for credentials |
| PR.AC-2 | Physical security: access cards, biometrics |
| PR.AC-3 | Remote access: VPN, MFA |
| PR.AC-4 | Least privilege and separation of duties |
| PR.AC-5 | Network integrity: firewalls, IDS/IPS, segmentation |

**Policy Hierarchy:** Policy → Standard → Guideline → Procedure

**Key Concepts:** Risk strategies · NIST CSF · PR.AC · Least privilege · Policy vs standard vs guideline

---

## 🛠️ Tools & Technologies Used

`Kali Linux` · `Ubuntu` · `VirtualBox` · `Scapy` · `Wireshark` · `Mimikatz` · `John the Ripper` · `crunch` · `ScoutSuite` · `Pacu` · `Nmap` · `Metasploitable` · `Snort` · `WebGoat` · `AlienVault/Security Onion (SIEM)` · `OWASP ZAP` · `Python venv` · `AWS CLI`

---

*Portfolio maintained by [Oladapo Afolabi] · [https://www.linkedin.com/in/oladapo-afolabi-561834145/] · [oladapokafolabi@gmail.com]*
