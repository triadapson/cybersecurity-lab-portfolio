# 🖥️ Windows Administration & PowerShell Scripting — Lab Portfolio

A collection of hands-on labs focused on **Windows system administration**, **user management**, **data security**, and **PowerShell scripting**. These labs build practical skills directly applicable to IT administration and cybersecurity roles.

All screenshots to Labs can be found here : https://docs.google.com/document/d/1dJcwWXBFHc-UGEdxF3VCT_Qdcgkk74yjPqOGmZvcqok/edit?usp=drive_link
---

## 📋 Table of Contents

| # | Lab | Topics |
|---|-----|--------|
| 1 | [Windows 10 Installation](#lab-1-windows-10-installation) | Clean install, locale config, MDT, Sysprep, setup logs |
| 2 | [Configuring Users](#lab-2-configuring-users) | Local users & groups, policies, UAC, VPN, Remote Desktop |
| 3 | [Managing Data](#lab-3-managing-data) | NTFS permissions, OneDrive, BitLocker encryption |
| 4 | [Managing the Windows 10 Environment](#lab-4-managing-the-windows-10-environment) | Desktop config, virtual memory, power plans, services |
| 5 | [Configuring Network Connectivity](#lab-5-configuring-network-connectivity) | Network details, static IP, DHCP, domain join, Active Directory |
| 6 | [Configuring Recovery](#lab-6-configuring-recovery) | Safe mode, boot logging, backup/restore, system image, restore points |
| 7 | [Managing Devices](#lab-7-managing-devices) | FAT32 to NTFS, disk quotas, volumes, GPT, dynamic disks, drive letters |
| 8 | [Managing Security](#lab-8-managing-security) | Windows Defender advanced scans, firewall rules, Application Guard, Credential Guard, Exploit Guard |
| 9 | [Working with PowerShell](#lab-9-working-with-powershell) | DOS commands, processes, execution policy, providers, scripting, variables, loops, conditionals |

---

## Lab 1: Windows 10 Installation

**Objective:** Perform a clean installation of Windows 10, configure system settings, troubleshoot failed installations, and use deployment tools (MDT and Sysprep) for enterprise imaging.

**Exercises:**

| Exercise | Description |
|----------|-------------|
| 1.1 | Performed a clean install of Windows 10 from scratch |
| 1.3 | Configured locale settings (language, region, time zone) |
| 1.4 | Troubleshot failed installations using Windows Setup logs |
| 1.5 | Downloaded and installed Microsoft Deployment Toolkit (MDT) |
| 1.6 | Configured MDT for automated OS deployments |
| 1.7 | Prepared a system for imaging using the System Preparation Tool (Sysprep) |

**Tools Used:** Windows 10 Setup · Microsoft Deployment Toolkit (MDT) · Sysprep · Windows Setup Logs

**Key Concepts:** Clean OS installation · Locale configuration · Deployment automation · System imaging · Setup log analysis

---

## Lab 2: Configuring Users

**Objective:** Manage local user accounts and groups, configure security policies, and set up remote access in a Windows environment.

**Exercises:**

| Exercise | Description |
|----------|-------------|
| 2.1 | Added the Local Users and Groups snap-in via MMC |
| 2.2 | Accessed Local Users and Groups through Computer Management |
| 2.3 | Created new user accounts via the MMC console |
| 2.4 | Disabled user accounts |
| 2.5 | Deleted user accounts |
| 2.6 | Renamed user accounts |
| 2.7 | Changed user passwords |
| 2.8 | Added users to existing groups |
| 2.9 | Set up user profiles |
| 2.10 | Assigned home folders to user accounts |
| 2.11 | Created local groups |
| 2.12 | Added accounts to groups |
| 2.13 | Added the Local Computer Policy snap-in to MMC |
| 2.14 | Accessed and navigated Local Group Policy Objects (LGPO) |
| 2.15 | Configured password policies (complexity, length, expiration) |
| 2.16 | Configured account lockout policies |
| 2.17 | Configured audit policies for security event logging |
| 2.18 | Applied user-rights policies |
| 2.19 | Observed how UAC (User Account Control) affects standard vs. admin accounts |
| 2.20 | Enabled and configured Remote Desktop |
| 2.21 | Set up a VPN connection |

**Tools Used:** MMC · Computer Management · Local Group Policy Editor (gpedit.msc) · Remote Desktop · VPN

**Key Concepts:** User account lifecycle · Group management · Password & lockout policies · Audit policies · UAC · Remote access · VPN setup

---

## Lab 3: Managing Data

**Objective:** Secure and manage data using NTFS permissions, cloud storage (OneDrive), and full-disk encryption (BitLocker).

**Exercises:**

| Exercise | Description |
|----------|-------------|
| 3.1 | Configured and managed NTFS file/folder permissions |
| 3.2 | Logged into and configured OneDrive for cloud file storage |
| 3.3 | Enabled and configured BitLocker drive encryption on Windows 10 |

**Tools Used:** Windows Explorer (NTFS Permissions) · OneDrive · BitLocker

**Key Concepts:** NTFS permission model · Principle of least privilege · Cloud storage integration · Full-disk encryption · Data protection

---

## Lab 4: Managing the Windows 10 Environment

**Objective:** Customize and optimize the Windows 10 environment including desktop settings, system performance, power management, and background services.

**Exercises:**

| Exercise | Description |
|----------|-------------|
| 4.1 | Configured Windows 10 desktop options (themes, display, taskbar) |
| 4.2 | Installed new Windows features via Settings |
| 4.3 | Changed the computer name |
| 4.4 | Adjusted virtual memory (paging file) settings for performance optimization |
| 4.5 | Configured a custom power plan |
| 4.6 | Configured the power button to trigger Hibernate mode |
| 4.7 | Managed Windows services (startup type, running/stopped states) |

**Tools Used:** Windows Settings · System Properties · Services (services.msc) · Power Options

**Key Concepts:** System optimization · Virtual memory management · Power plans · Hibernate · Windows services lifecycle

---

## Lab 5: Configuring Network Connectivity

**Objective:** Configure and manage network connections in Windows 10, including wireless settings, static/dynamic IP addressing, and domain integration.

**Exercises:**

| Exercise | Description |
|----------|-------------|
| 6.1 | Viewed detailed network connection properties |
| 6.2 | Viewed wireless network connection properties |
| 6.3 | Accessed and configured Windows 10 wireless network properties |
| 6.4 | Configured a static TCP/IP address |
| 6.5 | Configured DHCP for automatic IP address assignment |
| 6.6 | Connected a Windows 10 machine to a domain |
| 6.7 | Added Windows 10 to the domain via Active Directory |

**Tools Used:** Network & Sharing Center · Network Adapter Settings · Active Directory · ipconfig

**Key Concepts:** Static vs. dynamic IP addressing · DHCP · Wireless network configuration · Domain joining · Active Directory integration

---

## Lab 6: Configuring Recovery

**Objective:** Use Windows recovery tools to troubleshoot boot issues, back up and restore data, and create system images and restore points.

**Exercises:**

| Exercise | Description |
|----------|-------------|
| 7.1 | Booted the computer into Safe Mode |
| 7.2 | Enabled and used boot logging to diagnose startup issues |
| 7.3 | Backed up files using Windows Backup |
| 7.4 | Restored files from a backup |
| 7.5 | Configured OneDrive for automatic cloud backup |
| 7.6 | Created a full system image backup |
| 7.7 | Practiced creating a second system image |
| 7.8 | Restored the system using a restore point |
| 7.9 | Recovered deleted files using the Recycle Bin |

**Tools Used:** Windows Recovery Environment · Safe Mode · Boot Log · Backup and Restore · OneDrive · System Image · System Restore

**Key Concepts:** Safe mode diagnostics · Boot logging · File backup & restore · System imaging · Restore points · Cloud backup

---

## Lab 7: Managing Devices

**Objective:** Manage disk partitions, file systems, volumes, and storage configurations using Windows Disk Management tools.

**Exercises:**

| Exercise | Description |
|----------|-------------|
| 10.1 | Converted a FAT32 partition to NTFS using the `convert` command |
| 10.2 | Configured disk quotas to limit storage usage per user |
| 10.3 | Configured OneDrive for cloud storage integration |
| 10.4 | Added a Disk Management snap-in via MMC |
| 10.5 | Created a new simple volume on an unallocated disk |
| 10.6 | Converted a basic disk to a GPT (GUID Partition Table) disk |
| 10.7 | Converted a basic disk to a dynamic disk |
| 10.8 | Edited a drive letter (changed drive F: → H:) |
| 10.9 | Deleted a partition (removed Simple Volume H:) |
| 10.10 | Created an extended volume across disk space |

**Tools Used:** Disk Management (diskmgmt.msc) · MMC · `convert` command · OneDrive

**Key Concepts:** FAT32 vs. NTFS · Disk quotas · GPT vs. MBR · Basic vs. dynamic disks · Volume management

---

## Lab 8: Managing Security

**Objective:** Harden Windows security using Windows Defender tools including advanced scanning, firewall rules, Application Guard, Credential Guard, and Exploit Guard.

**Exercises:**

| Exercise | Description |
|----------|-------------|
| 12.1 | Ran an advanced malware scan using Windows Defender |
| 12.2 | Created a new inbound firewall rule using Windows Defender Firewall with Advanced Security |
| 12.3 | Installed Windows Defender Application Guard |
| 12.4 | Used Windows Defender Application Guard to browse in an isolated container |
| 12.5 | Configured Windows Defender Application Guard for enterprise environments |
| 12.6 | Enabled and configured Windows Defender Credential Guard |
| 12.7 | Configured Windows Defender Exploit Guard to reduce attack surface |

**Tools Used:** Windows Defender · Windows Defender Firewall with Advanced Security · Application Guard · Credential Guard · Exploit Guard

**Key Concepts:** Advanced malware scanning · Inbound firewall rules · Containerized browsing · Credential protection · Exploit mitigation

---

## Lab 9: Working with PowerShell

**Objective:** Develop practical PowerShell scripting skills from basic commands through variables, conditionals, and loops.

**Exercises:**

| Exercise | Description |
|----------|-------------|
| 1.2.1 | Used DOS commands within PowerShell |
| 1.2.2 | Managed running processes using PowerShell |
| 1.2.3 | Used `-WhatIf` and `-Confirm` options |
| 1.3.1 | Configured PowerShell execution policies |
| 2.2.1 | Created and customized PowerShell profile scripts |
| 2.5.1 | Viewed and navigated PowerShell providers |
| 3.1.1 | Created and executed a basic PowerShell script |
| 3.3.1 | Viewed and explored PowerShell variables |
| 3.7.1 | Compared data using comparison operators |
| 3.7.2 | Used `if` constructs for conditional logic |
| 3.7.3 | Used `switch` constructs for multi-branch logic |
| 3.8.1 | Used `foreach` loops to iterate over collections |
| 3.8.2 | Used `for` loops for index-based iteration |

**Tools Used:** PowerShell ISE · PowerShell Terminal · `.ps1` script files

**Key Concepts:** Execution policy · Process management · Variables · Conditionals · Loops · Script authoring

---

## 🛠️ Tools & Technologies Used

`Windows 10` · `MMC` · `MDT` · `Sysprep` · `Local Group Policy Editor` · `BitLocker` · `OneDrive` · `NTFS Permissions` · `UAC` · `PowerShell ISE` · `Active Directory` · `Windows Defender` · `Disk Management`

---

*Portfolio maintained by [Oladapo Afolabi] · [https://www.linkedin.com/in/oladapo-afolabi-561834145/] · [oladapokafolabi@gmail.com]*
