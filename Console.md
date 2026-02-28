<img width="1929" height="911" alt="image" src="https://github.com/user-attachments/assets/de8de32e-bedf-4b6b-a021-b0f5ec00e198" />
Establish a console connection to a Cisco device using a USB-to-Serial cable inside a Windows virtual machine.

Environment:

-VMware Workstation

-Windows 10 VM ("Joker")

-PuTTY

-USB-to-Serial Console Cable

-Cisco Catalyst device

Steps Taken:

-Plugged USB-to-Serial console cable into host machine.

-Passed USB device into VMware virtual machine.

-Opened Device Manager inside VM.

Verified console cable was detected as:
USB Serial Port (COM3)

-Opened PuTTY and selected:

-Connection Type: Serial

-Speed: 9600

Adjusted serial line to match detected COM port:
-COM3
