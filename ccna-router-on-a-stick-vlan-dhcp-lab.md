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

<img width="2206" height="891" alt="image" src="https://github.com/user-attachments/assets/fc6f62ac-4d70-4844-888a-e685d11254cb" />


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
```

## 🔀 Subinterfaces 

```bash
interface g0/0/0.10
 encapsulation dot1Q 10
 ip address 192.168.50.1 255.255.255.192

interface g0/0/0.20
 encapsulation dot1Q 20
 ip address 192.168.50.65 255.255.255.192

interface g0/0/0.30
 encapsulation dot1Q 30
 ip address 192.168.50.129 255.255.255.192

interface g0/0/0.40
 encapsulation dot1Q 40
 ip address 192.168.50.193 255.255.255.192
```

## 🔀 Internet Interface

```bash
interface g0/0/1
ip address 11.0.0.50 255.255.255.0
no shutdown
```

## DHCP Configuration

```bash
ip dhcp pool VLAN10
network 192.168.50.0 255.255.255.192
default-router 192.168.50.1
dns-server 8.8.8.8
```


# Switch Configuration

## VLAN Creation

```bash
vlan 10
vlan 20
vlan 30
vlan 40
```

## Trunk Ports

```bash
interface g0/1
 switchport mode trunk
 switchport trunk allowed vlan 10,20,30,40
```

# Verification

## Routing Table

### Routing Table

<img width="966" height="870" alt="image" src="https://github.com/user-attachments/assets/6a592546-c059-49f9-9e94-36b2e38db379" />

```bash
show ip route
```

### DHCP Bindings

<img width="933" height="358" alt="image" src="https://github.com/user-attachments/assets/f2b890ac-cfe9-4fb3-b564-4fabcd91bede" />

```bash
show ip dhcp binding
```

### Trunk Verification

<img width="939" height="707" alt="image" src="https://github.com/user-attachments/assets/de602772-e332-4dec-831a-fe8aef1cf74c" />

```bash
show interfaces trunk
```
