# Router-on-a-Stick VLAN & DHCP Lab (Cisco Packet Tracer)

## 📌 Overview

This lab demonstrates:

- VLAN segmentation
- Router-on-a-Stick configuration
- Inter-VLAN routing
- DHCP configuration for multiple subnets
- Switch trunking
- Static default routing
- Internet connectivity simulation

The network was subnetted using /26 networks from 192.168.50.0/24.

---

## 🖥️ Network Topology

![Topology Screenshot](images/topology.png)

---

## 🌐 IP Addressing Scheme

| VLAN | Subnet | Gateway |
|------|--------|----------|
| VLAN 10 | 192.168.50.0/26 | 192.168.50.1 |
| VLAN 20 | 192.168.50.64/26 | 192.168.50.65 |
| VLAN 30 | 192.168.50.128/26 | 192.168.50.129 |
| VLAN 40 | 192.168.50.192/26 | 192.168.50.193 |
| Internet | 11.0.0.0/24 | 11.0.0.254 |

---

## 🔀 Router Configuration (R1)

### Physical Interface

```bash
interface g0/0/0
 no ip address
 no shutdown
