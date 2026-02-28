<img width="1929" height="911" alt="image" src="https://github.com/user-attachments/assets/de8de32e-bedf-4b6b-a021-b0f5ec00e198" />
Establish a console connection to a Cisco device using a USB-to-Serial cable inside a Windows virtual machine.
## 🔌 Device Manager – Verifying Console COM Port

### 🎯 Objective

Verify that the USB-to-Serial console cable is properly detected inside the virtual machine and identify the assigned COM port.

---

### 🖥️ Environment

- VMware Workstation
- Windows 10 Virtual Machine
- USB-to-Serial Console Cable
- PuTTY (for serial connection)

---

### 🔎 Steps Performed

1. Connected the USB-to-Serial console cable to the host machine.
2. Passed the USB device into the VMware virtual machine.
3. Opened **Device Manager** inside the Windows VM.
4. Expanded:

   ```
   Ports (COM & LPT)
   ```

5. Verified that the console cable appeared as:

   ```
   USB Serial Port (COM3)
   ```

---

### 🧠 Why This Step Is Important

PuTTY must be configured to use the exact COM port assigned by Windows.

If PuTTY is set to a different COM port (example: COM1 instead of COM3), the console connection will fail.

---

### ⚠️ Common Issue

If the USB Serial Port does not appear:

- The USB device may not be connected to the VM
- VMware USB passthrough may not be enabled
- Drivers may not be installed

---

### 🚀 Result

Confirmed that the console cable was assigned:

```
COM3
```

This COM port was then used in PuTTY for establishing the serial console connection at 9600 baud rate.
