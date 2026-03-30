# 🌐 Network+ Labs — Portfolio

Hands-on networking labs covering core **CompTIA Network+** concepts including topology, subnetting, routing, switching, VLANs, security, and troubleshooting using Cisco Packet Tracer.

All screenshots to Labs can be found here : https://docs.google.com/document/d/1d0q29zECAxdTqzeALpOiMSZGqEIgqBHx/edit?usp=drive_link&ouid=102757233326623178029&rtpof=true&sd=true
---

## 📋 Table of Contents

| # | Lab | Topics |
|---|-----|--------|
| 1 | Introduction to Networks | Topology, ping connectivity |
| 2 | Conversions | Binary, decimal, hexadecimal |
| 3 | Internetworking | Switch & router config, multi-device pings |
| 4 | Subnetting | IPv4 CIDR, subnet masks, host ranges |
| 5 | Static and Dynamic Routing | Static routes, dynamic protocols |
| 6A/B | Switching, VLAN & Trunking | VLANs, trunking, inter-VLAN routing |
| 7 | Configuring Syslog | Syslog server, timestamped logging |
| 8 | Switchport Security | MAC-based port security, rogue prevention |
| 9 | Physical Security & Cloud | Data center, cloud, network availability |
| 10 | Troubleshooting | VLAN & trunking fault diagnosis |

---

## Lab 1: Introduction to Networks
Configured basic network topology and verified end-to-end connectivity using ping between PCs, laptops, and switches.

**Tools:** Cisco Packet Tracer · `ping`

## Lab 2: Conversions
Converted IP addresses between decimal/binary/hexadecimal, identified invalid IP addresses.

## Lab 3: Internetworking
Configured S1, S2 switches and R1 router. Verified routing between network segments.

**Tools:** Cisco Packet Tracer · Router/Switch CLI · `ping`

## Lab 4: Subnetting
Calculated subnets for /19, /22, /24, /27, /28, /29, /30 prefixes. Applied VLSM.

**Key Concepts:** CIDR · Subnet masks · Host range calculation · VLSM

## Lab 5: Static and Dynamic Routing
Configured R1/R2/R3 with static routes then dynamic routing. Verified convergence.

## Lab 6A/B: Switching, VLAN & Trunking
Configured VLANs, trunk links, and inter-VLAN routing (router-on-a-stick).

- Same VLAN pings: **successful**
- Different VLAN pings before routing: **unsuccessful**
- After inter-VLAN routing: **successful**

## Lab 7: Configuring Syslog
Configured switch and router to send logs to a Syslog server with timestamps.

## Lab 8: Switchport Security
Implemented MAC address binding. Rogue laptop denied after security enabled. Legitimate PCs still communicated.

## Lab 9: Physical Security, Data Center & Cloud
Defined data sanitization terms, identified Spine/Leaf architecture, cloud elasticity, SNMP, NetFlow, Syslog.

## Lab 10: Troubleshooting
Diagnosed VLAN/trunking faults. Before fix: cross-VLAN pings failed. After correcting trunk configs: all pings successful.

---

## 🛠️ Tools & Technologies

`Cisco Packet Tracer` · `Switch CLI` · `Router CLI` · `VLANs` · `Trunking` · `Inter-VLAN Routing` · `Static Routing` · `Syslog` · `Switchport Security` · `SNMP` · `NetFlow` · `Subnetting` · `CIDR`

---

*Portfolio maintained by [Oladapo Afolabi] · [https://www.linkedin.com/in/oladapo-afolabi-561834145/] · [oladapokafolabi@gmail.com]*
