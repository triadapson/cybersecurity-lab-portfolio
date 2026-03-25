# 🔍 IT Security Forensics — Lab Portfolio

Hands-on digital forensics labs covering the complete **forensic investigation lifecycle** — from evidence acquisition and crime scene processing through file system analysis, steganography detection, email forensics, and VM investigations — using Autopsy, FTK Imager, OSForensics, and WinHex.

---

## 📋 Table of Contents

| # | Lab | Topics |
|---|-----|--------|
| 1 | Investigation Using Autopsy | Autopsy case investigation, metadata, workplace misconduct |
| 2 | The Investigator's Office and Laboratory | Forensics policy, CHFI certification, disaster recovery |
| 3 | Data Acquisition | Mini-WinFE, Linux vs Windows acquisition, FTK Imager |
| 4 | Processing Crime and Incident Scenes | OSForensics, MD5/SHA1 hashing, hash verification |
| 5 | Working with Windows and CLI Systems | WinHex, registry, password extraction |
| 6 | Current Digital Forensic Tools | EnCase, FTK, Nuix, EasyRecovery, hex editors |
| 7A/B | Linux and Macintosh File Systems | Mobile forensics, Autopsy vs OSForensics vs FTK Imager |
| 8 | Digital Forensics Analysis and Validation | File carving, image conversion, steganography detection |
| 9 | Virtual Machine Forensics, Live Acquisitions & Network Forensics | USB forensic lab, VM security |
| 10 | Email and Social Media Investigations | Aid4Mail, Outlook PST, Enron data, social media forensics |

---

## Lab 1: Investigation Using Autopsy

**Case:** Investigation of George's computer usage — workplace misconduct.

| Question | Finding |
|----------|---------|
| Disk acquisition | Company forensic department |
| Laptop owner | **Amelia Phillips** (from metadata) |
| File access times | Primarily at **14:50 EST** |
| Applicable policies | AUP, Email/Internet Policy, Data Protection, Resource Abuse Policy |
| Other findings | Domain records, meeting with Earl (Aug 18), client Excel spreadsheet with PII |

**Reflection:** Understood public sector (criminal investigation) vs private sector (policy violation) forensics, and requirements for admissible private sector investigations.

**Tools:** Autopsy · Disk image analysis

---

## Lab 2: The Investigator's Office and Laboratory

### Project 2-1 — Digital Investigation Policy (ABC Corp.)
- Purpose · Policy Statement · Definitions · 5-Step Process (Incident Response → Collection → Preservation → Analysis → Reporting)
- References: GDPR, CCPA, NIST SP 800-86, ISO/IEC 27037:2017

### Project 2-2 — CHFI Certification Research
- EC-Council (est. 1995), ANAB accredited, DoD approved
- Covers: evidence collection, forensic analysis, incident response, evidence presentation

### Project 2-4 — Disaster Recovery Plan (Acme Corp.)
- Risks: natural disasters, power outages, hardware failures, cyberattacks
- Backup schedule: daily incremental · weekly full · monthly archival · annual review
- Hardware/software inventory: FTK Imager, Autopsy, EnCase

---

## Lab 3: Data Acquisition

**Mini-WinFE:** Boots from removable media — collects evidence without altering original data.

| Factor | Linux | Windows |
|--------|-------|---------|
| Tools | `dd`, `rsync` (CLI) | FTK Imager, EnCase (GUI) |
| Live acquisition | Natively supported | Requires specialized tools |
| Filesystem support | Extensive (NTFS, FAT, Ext, HFS+) | NTFS, FAT32, exFAT |
| Cost | Free open-source | Commercial licensing |

**Hands-On:** Created forensic disk image from USB using FTK Imager — verified acquisition integrity.

**Tools:** FTK Imager · Mini-WinFE · `dd`

---

## Lab 4: Processing Crime and Incident Scenes

**Hash Verification Results:**

| File State | MD5 Hash | SHA1 Hash |
|-----------|----------|-----------|
| Original | `8e85440c4c1fb60300014db6bd2716a2` | `906ectree1a64f46645...` |
| After editing | `0f74de60505b5513abd81fa3537271f0` | `c6a6ca707e9046...` |

**Key observation:** Both hashes changed completely — proving hash verification detects even minor modifications.

**Tools:** OSForensics · MD5/SHA1 hashing

---

## Lab 5: Working with Windows and CLI Systems

- WinHex: each file has unique hex structure · can detect and reveal alterations
- Registry viewer: explored Windows registry hives and keys
- **OSForensics extracted passwords** from image files — including Wi-Fi passwords and browser-saved credentials
- Note: Trial version limited to 5 browser passwords

**Reflection:** "Nothing is truly hidden" — passwords believed safe in Chrome were extracted.

**Tools:** WinHex · OSForensics · Windows Registry Viewer

---

## Lab 6: Current Digital Forensic Tools

### Forensic Tool Comparison
| Category | EnCase | FTK | Nuix | EasyRecovery |
|----------|--------|-----|------|--------------|
| Acquisition | ✓ all modes | ✓ all modes | ✓ all modes | ✓ (no CLI/remote) |
| Decryption | ✓ | ✓ | ✓ | ✗ |
| Scripting | ✓ | ✓ | ✓ | ✗ |
| E-Discovery | ✓ | ✓ | ✓ | ✗ |

**Hex Editors:** Mac: 0xED · Hex Fiend (up to 118GB). Linux: HxD · Okteta

**Validation Procedure:** ISO 17025:2017 standards — installation, functionality, benchmarking, integrity, documentation.

---

## Lab 7A/B: Linux and Macintosh File Systems

### Mobile Tool Comparison
| Feature | Cellebrite UFED | Magnet AXIOM | Oxygen Forensic |
|---------|----------------|--------------|------------------|
| Price | $6,000–$15,000 | $3,000–$6,000 | $2,000–$4,000 |
| Cloud Access | Yes | Yes | Yes |
| Unique Strength | Wide device support | Timeline + geolocation | Mobile extraction |

**Recommended:** Magnet AXIOM — best balance of features, updates, and pricing.

### Free Tool Comparison
| Feature | Autopsy | OSForensics | FTK Imager |
|---------|---------|-------------|------------|
| Email Analysis | Yes | Yes | No |
| Timeline | Yes | Yes | No |
| Reporting | HTML, CSV | HTML, CSV | None native |
| Plugins | Yes | Few | No |

---

## Lab 8: Digital Forensics Analysis and Validation

### File Carving
- C08frag: used `jfif` keyword — recovered hidden JPGs from fragmented disk
- C08carve: used `zzzz` keyword — recovered JPGs from unallocated space

### Image Format Conversions
| Conversion | Size Change |
|-----------|-------------|
| SPIDER.bmp → Spider.jpg | 1.03MB → 48.5KB (quality loss) |
| FLOWER.gif → Flower.jpg | 318KB → 98.8KB (transparency lost) |
| Cartoon.bmp → Cartoon.gif | 18.2KB → 10.4KB |

### Steganography Detection (Mission.bmp vs Mission-steg.bmp)
10 byte-level differences found at offsets ED, 209, 27E, 3C5, 509, etc. — all ±1 deviation.

**Conclusion:** **LSB (Least Significant Bit) steganography** used — data embedded without visible image changes.

### Hash Databases
- Circular left rotation encryption: **not reliable** (easily reversible)
- Hashes added to `Special Project-A` database in Autopsy
- Report generated from `Superior-Personnel-Records` tag

**Tools:** Autopsy · IrfanView · S-Tools4 · WinHex

---

## Lab 9: Virtual Machine Forensics, Live Acquisitions & Network Forensics

### USB-Based Forensic Lab
**Hypervisors:** VirtualBox · VMware Workstation Player · Hyper-V

**Forensic tools on USB:** Autopsy · FTK Imager · DFF · OSForensics · EnCase · SIFT · Volatility · Plaso · Rekall · X-Ways

### VM Security Best Practices (10 items)
1. VM snapshot before distribution · 2. Remove sensitive data · 3. Licensing mechanisms · 4. Encrypt disk image · 5. Strong passwords · 6. Disable unnecessary services · 7. Time-limited usage · 8. Usage monitoring · 9. Clear documentation · 10. Regular patching

---

## Lab 10: Email and Social Media Investigations

### Aid4Mail — Eric Saibi PST Investigation
1. Installed Aid4Mail · 2. Copied `Eric_saibi.pst` · 3. Selected Outlook PST source · 4. Applied filters · 5. Exported to CSV · 6. Analysed data

**Findings:** Personal PII identified (names, addresses, phone numbers) · **Enron scandal** emails (financial transactions)

### Social Media Forensic Scenario (Facebook Threat)
1. Gather message info (sender, content, timestamp)
2. Report to administration + mental health services
3. **FTK Imager** — forensic image of Facebook data
4. **Autopsy** — metadata, IP, browser cookies to locate sender
5. Keyword search + regex for threat content
6. Hash verification of evidence
7. Document and preserve for legal proceedings

**Tools:** Aid4Mail · Autopsy · FTK Imager · Outlook PST · CSV analysis

---

## 🛠️ Tools & Technologies Used

`Autopsy` · `FTK Imager` · `OSForensics` · `WinHex` · `EnCase` · `Nuix` · `Ontrack EasyRecovery` · `Magnet AXIOM` · `Cellebrite UFED` · `Oxygen Forensic Detective` · `Aid4Mail` · `IrfanView` · `S-Tools4` · `Volatility` · `VirtualBox` · `VMware` · `Mini-WinFE` · `0xED` · `Hex Fiend` · `HxD` · `Okteta` · `Kali Linux` · `MD5/SHA1 hashing` · `LSB steganography detection`

---

*Portfolio maintained by [Oladapo Afolabi] · [https://www.linkedin.com/in/oladapo-afolabi-561834145/] · [oladapokafolabi@gmail.com]*
