# 🔵 Cisco Technologies (CCNA) — Lab Portfolio

Hands-on labs covering **Cisco CCNA** concepts completed on physical Cisco Catalyst switches and 4221 routers as well as Cisco Packet Tracer.

Screenshots to all Labs can be found here https://docs.google.com/document/d/1a_m4fAbAlRFIw82M0fXwcdGWlWA6ssO8/edit?usp=drive_link&ouid=102757233326623178029&rtpof=true&sd=true

---

## 📋 Table of Contents

| # | Lab | Topics |
|---|-----|--------|
| 1 | Initial Configuration — Switches & Router | LAN/WAN setup, basic config, console access |
| 2 | DHCP Configuration (Local and Remote) | Local DHCP, DHCP relay (ip helper-address) |
| 3 | Subnetting | /24 and /16 subnet design scenarios |
| 4 | Subnetting Implementation | VLSM design & physical implementation |
| 5 | Dynamic Routing Using OSPF | OSPFv2 config, neighbour relationships |
| 6 | Configure OSPFv2 Routing and Verification | Full OSPFv2, show commands, ping verification |
| 7 | Configure OSPFv3 Routing and Verification | OSPFv3 IPv6 routing, show ipv6 commands |
| 8 | STP and EtherChannel | STP root bridge, LACP EtherChannel |
| 9 | Access Control List Configuration | Standard & extended ACLs, permit/deny |
| 10 | Configuring NAT | Static NAT, dynamic NAT, translations |
| 11 | Configuring PAT | PAT overload, port-based address translation |
| 12 | Configuring RADIUS | Local AAA auth, Telnet, RADIUS centralized |
| 13 | Configuration of HSRP | HSRP active/standby, failover testing |
| 14 | Configuring GRE Tunnels | GRE tunnel, routing over tunnel, traceroute |

---

## Lab 1: Initial Configuration — Switches & Router
**Hardware:** Cisco Catalyst 1000 switch · 2x Cisco 4221 routers · Console cables

**Activities:** Configured hostname, passwords, MOTD banner, management IP on S1. Router interfaces G0/0/1 (LAN) and S0/1/0 (WAN serial). Enabled SSH and console/VTY access. Verified connectivity.

**Key Concepts:** Basic switch/router config · LAN/WAN topology · Serial WAN links · SSH access

---

## Lab 2: DHCP Configuration (Local and Remote)
**Part 1 — Local DHCP:** R1/R2/R3 configured with DHCP pools. Full ping verification across all devices.

**Part 2 — Remote DHCP (IP Helper):** Configured `ip helper-address` for remote DHCP relay. End-to-end pings successful across both LAN segments.

**Tools:** `ip dhcp pool` · `ip helper-address` · `show ip dhcp binding`

---

## Lab 3: Subnetting
**Scenario 1** — /24, 3 subnets: borrowed 2 bits → 255.255.255.192 (/26), 62 hosts/subnet

**Scenario 2** — /24, 8 subnets: borrowed 3 bits → 255.255.255.224 (/27), 30 hosts/subnet

**Scenario 3** — /16, 15 subnets: borrowed 4 bits → 255.255.240.0 (/20), 4094 hosts/subnet

**Key Concepts:** Subnet bit borrowing · CIDR · VLSM design

---

## Lab 4: Subnetting Implementation
**Hardware:** 3x Cisco Catalyst 1000 switches · 3x Cisco 4221 routers

Designed VLSM addressing from `172.21.55.64/27`. Configured all 3 switches and routers. Verified full mesh connectivity.

---

## Lab 5: Dynamic Routing Using OSPF
Configured OSPFv2 on multiple routers. Verified neighbour adjacency (`show ip ospf neighbor`), routing tables (`show ip route`), end-to-end connectivity.

**Key Concepts:** OSPFv2 · OSPF process ID · Area 0 · DR/BDR election

---

## Lab 6: Configure OSPFv2 Routing and Verification
**Topology:** 4 routers (R1–R4), 2 switches, 4 PCs with serial WAN links.

**Verification:** Pings from all devices to all destinations ✓

**Show commands on all 4 routers:** `show ip route` · `show ip ospf neighbor` · `show ip ospf` · `show ip interface brief`

---

## Lab 7: Configure OSPFv3 Routing and Verification
**Topology:** 4 routers (R1–R4), 4 multilayer switches, 4 PCs with IPv6 addressing.

**Show commands:** `show ipv6 route` · `show ipv6 ospf neighbor` · `show ipv6 protocols` · `show ipv6 ospf interfaces`

**Key Concepts:** OSPFv3 for IPv6 · IPv6 routing table · OSPFv3 vs OSPFv2

---

## Lab 8: STP and EtherChannel
### STP Analysis (3 switches in triangle topology)
| Question | Answer |
|----------|--------|
| Root Bridge elected | **S3** (lowest MAC: 0005.5E79.4C37) |
| Root port on S1 | f0/4 |
| Root port on S2 | f0/4 |
| Blocked port | S2 f0/2 |

### LACP EtherChannel
Configured LACP EtherChannel on S1, S2, S3. Verified with `show etherchannel summary` and `show interfaces trunk`.

**Key Concepts:** STP root bridge · MAC address tie-breaking · Blocked ports · LACP · Port-channel

---

## Lab 9: Access Control List Configuration
**Topology:** 3 routers, 4 switches, PCs, Web Server, File Server

**ACL Results after implementation:**
- S1 → File Server: ✓ Permitted
- S1 → Web Server: ✗ Denied
- S2 → File Server: ✗ Denied
- S2 → Web Server: ✓ Permitted

**Tools:** `access-list` · `ip access-group` · `show access-list`

---

## Lab 10: Configuring NAT
**Topology:** S1 switch, Gateway router, ISP router, PC-A, PC-B

- Static NAT: PC-A mapped to public IP — ping from/to ISP ✓
- Dynamic NAT: pool-based NAT — pings from PC-A and PC-B ✓
- Verified: `show ip nat translations` · `show ip nat statistics`

**Key Concepts:** Static/dynamic NAT · Inside local/global addresses · NAT translation table

---

## Lab 11: Configuring PAT
**Activities:** NAT pool overload — 3 PCs sharing public IPs. PAT with single public IP. Cleared NAT table with `clear ip nat trans *`.

**Reflection:** PAT uses unique source port numbers per session so multiple devices share one public IP.

**Tools:** `ip nat inside source list overload` · `show ip nat statistics`

---

## Lab 12: Configuring RADIUS
**Part 1** — Basic device setup, encrypted passwords
**Part 2** — Local user accounts, Telnet from PC-A to R1 (fixed with `transport input telnet`)
**Part 3** — AAA on R3 with `aaa new-model`, hashed secrets, tested invalid user (denied)
**Part 4** — Centralized RADIUS server, new user login successful, logs verified

**Tools:** `aaa new-model` · `aaa authentication login` · `radius-server host`

---

## Lab 13: Configuration of HSRP
**Tasks:** STP → OSPF → HSRP group configured — BR_R1 Active, BR_R2 Standby

**Failover test:** Shutdown G0/0 on BR_R1 → BR_R2 automatically became Active. Ping continued with minimal interruption ✓

**Simulation mode:** HSRP Hello packets observed on both routers. Traffic rerouted when cable deleted.

**Tools:** `standby` · `show standby brief` · Packet Tracer Simulation Mode

---

## Lab 14: Configuring GRE Tunnels
**Topology:** West ↔ ISP ↔ East with PC-A and PC-C at each site

**Part 1:** Physical interfaces configured, ping to default gateways ✓
**Part 2:** `interface tunnel 0` configured on West and East, tunnel Up/Up ✓
**Part 3:** OSPF over tunnel — `show ip route` shows tunnel routes. Traceroute confirmed traffic traverses GRE tunnel ✓

**Tools:** `interface tunnel` · `tunnel source` · `tunnel destination` · `show interfaces tunnel` · `traceroute`

---

## 🛠️ Tools & Technologies Used

`Cisco IOS CLI` · `Cisco Catalyst 1000` · `Cisco 4221` · `Cisco Packet Tracer` · `OSPFv2` · `OSPFv3` · `DHCP` · `ip helper-address` · `VLSM` · `Serial WAN` · `SSH` · `Telnet` · `STP` · `LACP EtherChannel` · `Standard/Extended ACLs` · `Static/Dynamic NAT` · `PAT` · `AAA` · `RADIUS` · `HSRP` · `GRE Tunnels` · `ping` · `traceroute` · `show ip route` · `show ip ospf` · `show spanning-tree` · `show etherchannel summary` · `show ip nat translations` · `show standby`

---

*Portfolio maintained by [Oladapo Afolabi] · [https://www.linkedin.com/in/oladapo-afolabi-561834145/] · [oladapokafolabi@gmail.com]*
