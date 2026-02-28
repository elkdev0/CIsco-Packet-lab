# 🖧 Assigning IP Address to Router Interface (G0/0)

## 📌 Problem

The router interface `GigabitEthernet0/0` had:

- No IP address assigned
- Interface in shutdown state

Observed configuration:

```bash
interface GigabitEthernet0/0
 no ip address
 shutdown
```

This prevents Layer 3 communication.

---

## 🔧 Solution

Entered interface configuration mode:

```bash
interface g0/0
```

Assigned IP address:

```bash
ip address 192.168.2.1 255.255.255.0
```

Enabled the interface:

```bash
no shutdown
```

---

## 🚀 Verification

```bash
show ip interface brief
```

Expected output:

```bash
GigabitEthernet0/0  192.168.2.1  YES manual  up  up
```

---

## 🧠 Key Takeaways

- Router interfaces are shutdown by default.
- Router interfaces do not have IP addresses by default.
- `no shutdown` is required to activate the interface.
