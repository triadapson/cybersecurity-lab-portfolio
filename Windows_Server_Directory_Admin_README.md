# 🖥️ Windows Server & Directory Administration — Lab Portfolio

A collection of hands-on labs focused on **Windows Server 2019 administration**, covering server installation, Active Directory, Hyper-V virtualization, resource access, printing, and storage management.

---

## 📋 Table of Contents

| # | Lab | Topics |
|---|-----|--------|
| 1 | Windows Server Installation & Post-Installation Tasks | Install, post-setup |
| 2 | Server Manager Configuration & Command Shell | Server Manager, WMI, PowerShell |
| 3 | Implementing Hyper-V & Rapid Server Deployment | Virtual switches, WDS, VM templates |
| 4 | Active Directory Installation & Exploration | AD DS, domain setup, sites, RODC |
| 5 | Configuring Resource Access | NFS, DFS, NTFS, EFS, auditing |
| 6 | Configuring Printing | Print server, print queues, troubleshooting |
| 7 | Configuring & Managing Data Storage | RAID, Storage Spaces, iSCSI, backup |
| 8 | Configuring & Managing Network Services | DNS, WINS, DHCP, failover |
| 9 | Configuring & Managing Remote Access Services | VPN, RADIUS, DirectAccess, RDS |
| 10 | Configuring Web Services & Cloud Technologies | IIS, Containers, WSL, Nano Server |
| 11 | Managing & Securing Windows Networks | Group Policy, AD CS, 802.1X, WSUS |
| 12 | Monitoring & Troubleshooting Windows Server 2019 | Performance Monitor, Event Viewer, tracert |

---

## Lab 1: Windows Server Installation & Post-Installation Tasks
**Activities:** Full Windows Server 2019 installation · Installed Google Chrome post-installation

**Tools:** Windows Server 2019 Setup · Server Manager

---

## Lab 2: Server Manager Configuration & Command Shell
**Activities:** Server Manager dashboard · Windows Admin Center · PowerShell cmdlets · PSProviders · WMI queries · PowerShell scripts

**Tools:** Server Manager · Windows Admin Center · PowerShell · WMI

---

## Lab 3: Implementing Hyper-V & Rapid Server Deployment
**Activities:** Virtual switch creation · WDS configuration · OS deployment · VM templates · VM hardware settings

**Tools:** Hyper-V Manager · WDS · Virtual Switch Manager

---

## Lab 4: Active Directory Installation & Exploration
**Activities:** AD DS install · Domain promotion (domain.com, DOMAINX, Windows Server 2008 level) · Forest functional level raised · Sites configured (ChicagoSite, ParisSite, TorontoSite, 180-min replication) · Users/groups managed · RODC deployed and removed

**Tools:** AD DS · ADUC · AD Sites and Services · AD Domains and Trusts

**Key Concepts:** Domain promotion · Functional levels · AD sites & replication · OUs · RODC

---

## Lab 5: Configuring Resource Access
**Activities:** NFS Server, FSRM, DFS Namespaces & Replication installed · NTFS permissions (Deny overrides Allow demonstrated) · EFS configured · NFS Advanced Sharing · DFS Replication verified · File screens and storage quotas applied

**Tools:** FSRM · DFS · NFS · EFS · PowerShell · Event Viewer

---

## Lab 6: Configuring Printing
**Activities:** Print Server installed · SamplePrinter1 and SamplePrinter2 configured · Printer notifications set · AD printer objects verified · Print queues managed · Print troubleshooting

**Tools:** Print Management Console · ADUC · Devices and Printers

---

## Lab 7: Configuring & Managing Data Storage
**Activities:** 4 virtual disks added · Simple volumes created · RAID-5 configured · Storage Spaces · iSCSI Target Server (iscsitarget1) · Scheduled backup of MarketingMaterials · File restore with overwrite

**Tools:** Disk Management · Storage Spaces · iSCSI Target · Windows Server Backup

**Key Concepts:** RAID-5 · Storage pools · iSCSI · Backup/restore

---

## Lab 8: Configuring & Managing Network Services
**Activities:** DNS zones created (zoneX.com) · nslookup verification · Secondary zones · WINS NetBIOS records · DHCP with name protection · DHCP failover configured

**Tools:** DNS Manager · nslookup · WINS · DHCP Manager

---

## Lab 9: Configuring & Managing Remote Access Services
**Activities:** VPN server (EAP + MS-CHAPv2) · VPN connected to 172.16.0.0/24 · RADIUS with daily log files · DirectAccess (A/AAAA records + 2 GPOs) · RDS roles (Web Access, Connection Broker, Session Host)

**Tools:** RRAS · NPS/RADIUS · DirectAccess · Remote Desktop Services

---

## Lab 10: Configuring Web Services & Cloud Technologies
**Activities:** IIS configured (http://FQDN/marketingapp) · Windows Containers (iiscontainer1-3 created and removed) · WSL web page update · LCOW (apachecontainer3) · Nano Server (Get-Service verified)

**Tools:** IIS Manager · Docker · WSL · LCOW · Nano Server

---

## Lab 11: Managing & Securing Windows Networks
**Activities:** GPO folder redirection · Default Domain Policy verified · AD Certificate Services (issued certs) · 802.1X WPA wireless · WSUS intranet update URLs · Defender firewall inbound rule

**Tools:** GPMC · AD CS · NPS · WSUS · Windows Defender Firewall

---

## Lab 12: Monitoring & Troubleshooting Windows Server 2019
**Activities:** Task Manager + Resource Monitor (10 screenshots) · Performance baseline at C:\Perflogs · Data Collector Sets (DataCollector01.blg, DataCollector02.etl) · Event Viewer (Critical/Error/Warning filtered) · tracert 1.1.1.1 · Advanced Boot Options + ntbtlog.txt

**Tools:** Task Manager · Resource Monitor · Performance Monitor · Event Viewer · tracert · nslookup

---

## 🛠️ Tools & Technologies Used

`Windows Server 2019` · `Server Manager` · `Windows Admin Center` · `Hyper-V` · `WDS` · `AD DS` · `ADUC` · `AD CS` · `PowerShell` · `WMI` · `NFS` · `DFS` · `FSRM` · `EFS` · `Disk Management` · `Storage Spaces` · `iSCSI` · `Windows Server Backup` · `RAID-5` · `DNS Manager` · `WINS` · `DHCP Manager` · `RRAS` · `NPS/RADIUS` · `DirectAccess` · `RDS` · `IIS` · `Docker` · `WSL` · `LCOW` · `Nano Server` · `GPMC` · `WSUS` · `Windows Defender Firewall` · `Performance Monitor` · `Event Viewer`

---

*Portfolio maintained by [Your Name] · [LinkedIn] · [Your Email]*
