# 🏢 VLAN Configuration – IT Department

## 🎯 Objective

Create a VLAN for the IT department and assign a switch port to it.

---

## 🔧 Step 1 – Create VLAN 20

```bash
vlan 20
name IT
```

---

## 🔧 Step 2 – Assign Port to VLAN

```bash
interface te1/0/1
switchport mode access
switchport access vlan 20
```

---

## 🔎 Verification

```bash
show vlan brief
```

Output:

```bash
20  IT  active  Te1/0/1
```

---

## 🧠 Key Learning

- VLANs provide Layer 2 segmentation.
- Access ports belong to one VLAN only.
- Devices connected to Te1/0/1 are now part of VLAN 20 (IT).
- This isolates broadcast domains between departments.







This lab demonstrates VLAN configuration and network segmentation using Cisco Packet Tracer.
Three VLANs were created to simulate departmental separation:

VLAN 10 – HR

VLAN 20 – IT

VLAN 30 – Sales

<img width="2178" height="1073" alt="vlan" src="https://github.com/user-attachments/assets/b522a337-25f8-4733-a8ca-bb79724298d9" />

<img width="1028" height="1035" alt="image" src="https://github.com/user-attachments/assets/559d9526-8119-4ed5-904b-7323d7578e41" />

<img width="2046" height="1028" alt="image" src="https://github.com/user-attachments/assets/8fcdc0f0-963a-4184-a416-542707dfdeb3" />
