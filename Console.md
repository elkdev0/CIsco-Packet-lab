<img width="1929" height="911" alt="image" src="https://github.com/user-attachments/assets/de8de32e-bedf-4b6b-a021-b0f5ec00e198" />
# 🔌 Console Access to Cisco Device Using PuTTY in VMware

## 🎯 Objective

Establish a console connection to a Cisco device using a USB-to-Serial cable inside a Windows virtual machine.

---

## 🖥️ Lab Environment

- VMware Workstation
- Windows 10 Virtual Machine ("Joker")
- PuTTY
- USB-to-Serial Console Cable
- Cisco Catalyst Switch

---

## 🔎 Overview

This lab demonstrates how to establish direct console access to a Cisco network device from within a virtualized Windows environment.

Console access is required for:

- Initial device configuration
- Password recovery
- Troubleshooting
- Out-of-band management

---

## 🧭 Steps Performed

### 1️⃣ Connect Console Cable

- Plugged USB-to-Serial console cable into host machine.
- Passed the USB device into the VMware virtual machine.

---

### 2️⃣ Verify COM Port in Device Manager

Opened **Device Manager** inside the Windows VM.

Navigated to:

```
Ports (COM & LPT)
```

Verified that the device appeared as:

```
USB Serial Port (COM3)
```

⚠️ This COM number is critical for PuTTY configuration.

---

### 3️⃣ Configure PuTTY

Opened PuTTY and configured the following:

Connection Type:
```
Serial
```

Serial Line:
```
COM3
```

Speed (Baud Rate):
```
9600
```

> Note: Cisco devices use 9600 baud rate by default for console connections.

---

### 4️⃣ Establish Console Session

Clicked **Open** in PuTTY.

Successfully accessed the Cisco CLI via console connection.

---

## ✅ Result

Console access was successfully established to the Cisco Catalyst device.

This enabled:

- Access to user EXEC mode
- Entry into privileged EXEC mode
- Device configuration from scratch

---

## 🧠 Key Learning

- The PuTTY serial port must match the COM port assigned in Device Manager.
- Cisco devices use 9600 baud rate by default.
- Serial mismatch is a common troubleshooting issue.
- Console access is essential for infrastructure-level configuration.

---

## 🏗️ Real-World Relevance

This process mirrors what:

- Data Center Technicians  
- NOC Engineers  
- Network Engineers  
- Infrastructure Engineers  

perform in production environments.

Engineers routinely:

- Verify COM ports
- Set correct baud rates
- Access devices via console
- Perform initial configurations

This lab reinforces real-world foundational networking skills.
