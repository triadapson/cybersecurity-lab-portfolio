# 🐧 Linux Administration — Lab Portfolio

Hands-on labs covering **Linux system administration** from installation and filesystem management through network services, cloud technologies, and database configuration. Completed on **Fedora Linux**.

---

## 📋 Table of Contents

| # | Lab | Topics |
|---|-----|--------|
| 2 | Linux Installation and Usage | Fedora install, BASH, KDE Plasma |
| 3 | Exploring Linux Filesystems | Navigation, vi editor, grep, wildcards |
| 4 | Linux Filesystem Management | mkdir, cp, mv, ln, chmod, chown |
| 5 | Linux Filesystem Administration | Partitions, mounting, quotas, fsck |
| 6 | Linux Server Deployment | systemctl, firewalld, dnf, RPM |
| 7 | Working with the BASH Shell | Scripting, variables, aliases, redirection |
| 8 | System Initialization, X Windows & Localization | Boot, systemd, GRUB, locale |
| 9 | Managing Linux Processes | ps, top, kill, cron, nice |
| 10 | Common Administrative Tasks | Users, groups, logging, password policies |
| 11 | Compression, System Backup & Software Installation | tar, gzip, dnf, RPM |
| 12 | Network Configuration | ifconfig, SSH, networkctl |
| 13 | Configuring Network Services & Cloud Technologies | DHCP, Apache, Samba, Postfix, PostgreSQL |

---

## Lab 2: Linux Installation and Usage
Installed Fedora Linux (password: LINUXrocks!). Explored BASH commands, case-sensitivity, installed KDE Plasma via `dnf groupinstall`, used `who`, `date`, command substitution.

**Tools:** Fedora Linux · BASH · `dnf` · KDE Plasma

---

## Lab 3: Exploring Linux Filesystems
Navigated absolute/relative paths. Viewed files with `cat`, `cat -n`, `tac`. Edited with `vi`. Used wildcard patterns and `grep` with regex (`t.e`, `^$`).

**Tools:** `cd` · `pwd` · `ls` · `cat` · `vi` · `grep`

---

## Lab 4: Linux Filesystem Management
Created dirs with `mkdir`, recursive copy with `cp -R`, renamed with `mv`, created hard links with `ln`. Set permissions with `chmod`, ownership with `chown`, configured `umask`.

**Tools:** `mkdir` · `cp` · `mv` · `ln` · `chmod` · `chown`

---

## Lab 5: Linux Filesystem Administration
Disk partitioning, mounting/unmounting, `/etc/fstab` configuration, disk quotas, `fsck` integrity checks, swap space management, LVM.

**Tools:** `fdisk` · `mount` · `fstab` · `quota` · `fsck` · `lvm`

---

## Lab 6: Linux Server Deployment
Server hostname setup, service management with `systemctl`, `firewalld` rules, package management with `dnf`/`rpm`, NTP with chrony, SSH hardening.

**Tools:** `systemctl` · `firewalld` · `dnf` · `rpm` · `chrony`

---

## Lab 7: Working with the BASH Shell
Shell variables, I/O redirection (`>`, `>>`, `<`), pipelines, aliases, BASH scripts with conditionals (`if`/`else`) and loops (`for`/`while`).

**Tools:** BASH · `export` · `alias` · `.sh` scripts

---

## Lab 8: System Initialization, X Windows & Localization
Modified GRUB boot parameters (single-user mode). Explored systemd targets. Managed X Windows and display managers. Configured locale with `localectl`.

**Tools:** GRUB · `systemctl` · `localectl` · `timedatectl`

---

## Lab 9: Managing Linux Processes
- `ps -el | less` — viewed process states
- `top` — interactive process monitoring
- `kill` with SIGTERM (signal 15)
- Created cron job: `/bin/false` at `30 20 * * *`
- `nice` and `renice` for priority adjustment

**Tools:** `ps` · `top` · `kill` · `crontab` · `nice`

---

## Lab 10: Common Administrative Tasks
- Created user `bozo` with UID, shell `/bin/bash`, home `/home/bozo`
- `chage -W 5 bozo` — password aging
- Locked/unlocked accounts — verified login at tty6
- `chown bozoette` — ownership change
- Viewed `logrotate` config in `/etc/logrotate.conf`

**Tools:** `useradd` · `passwd` · `chage` · `chown` · `/etc/shadow`

---

## Lab 11: Compression, System Backup & Software Installation
- Installed `ncompress` via `dnf`
- `tar -zcvf test2.tar.gz /etc/samba` — gzip compressed archive
- Compared compression ratios (gzip, bzip2, xz)
- RPM package queries and `dnf` group installs

**Tools:** `tar` · `gzip` · `bzip2` · `zip` · `dnf` · `rpm`

---

## Lab 12: Network Configuration
- `ifdown eth0; ifup eth0` — interface restart
- `networkctl` for systemd-networkd
- `ip addr` and `ifconfig` — interface info
- SSH: `ssh root@localhost` — verified with `who` and `ss -t`
- `ssh -X` for X11 forwarding

**Tools:** `ifconfig` · `ip` · `ss` · `ssh` · `networkctl`

---

## Lab 13: Configuring Network Services & Cloud Technologies
- **DHCP:** `dhcpd` configured and verified with `ps -ef | grep dhcpd`
- **Apache:** httpd configured, web page accessible at `http://FQDN/marketingapp`
- **Samba:** `/etc/samba/smb.conf` — tested with `testparm`, connected via `smbclient //127.0.0.1/root`
- **SFTP:** Uploaded `fstab` and `issue` to `/home/user1`, verified with `dir`
- **Postfix:** Email sent from `root` to `user1`, verified with `mail`
- **PostgreSQL:** Created `sales` database, `customer` table, granted ALL PRIVILEGES to `bob`

**Tools:** `dhcpd` · Apache `httpd` · Samba · SFTP · Postfix · PostgreSQL `psql`

---

## 🛠️ Tools & Technologies Used

`Fedora Linux` · `BASH` · `vi` · `grep` · `tar` · `gzip` · `dnf` · `rpm` · `systemctl` · `firewalld` · `crontab` · `ps` · `top` · `kill` · `ssh` · `ifconfig` · `networkctl` · `Apache httpd` · `Samba` · `Postfix` · `PostgreSQL` · `DHCP` · `SFTP` · `chmod` · `chown` · `useradd` · `LVM` · `fsck` · `GRUB`

---

*Portfolio maintained by [Your Name] · [LinkedIn] · [Your Email]*
