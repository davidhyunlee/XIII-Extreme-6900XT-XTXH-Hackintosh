# Maximus XIII Extreme / 10900K / 6900XT XTXH / OpenCore 0.7.7 Hackintosh

Build Specifications:  
ASUS Maximus XIII Extreme Z590 Motherboard.
Intel 10900K Comet Lake CPU
Corsair Vengeance DDR4 3600mhz CL14-16-16-36
XFX Radeon RX 6900XT Speedster Zero WB (XTXH Variant)
WD SN750/850 NVME Drives
Fenvi FV T919 Wireless Card
Motu M4 Audio Interface

Notes:

MacPro7,1 SMBIOS
The generated serial and UUID are not mine, however, I would suggest generating a new one in case someone else is using this config as-is.

USBMap.kext
This USB map has been custom made for the MacPro7,1 SMBIOS and mapped to every available USB port except the BIOS flashback USB port for the XIII Extreme.

SSDT-BRG0.aml
This SSDT is required to make the XTXH 6900XT card work.  This one is specifically compiled to work with the XIII Extreme.

NVMEFix.kext
This is not required if you are using the same NVME drives I have, the WD SN750 or SN850.  It actually caused issues when I tried using it.


What Works:
AirDrop / Handoff / AirPlay / Continuity
DRM
Bluetooth / Wi-Fi from Broadcom Chipset on Fenvi T919
Sleep
iMessage / Facetime

What Doesn't:
Built-in Intel Wi-fi and Bluetooth
Sidecar (due to SMBIOS choice. Using iMac20,2 enables SideCar but you lose DRM.  If you care more about Sidecar than DRM, switch to iMac20,1 or 20,2.)

Bugs:
Motu M4 audio interface doesn't always come back up after wake from sleep.  Turning the interface on and off fixes the issue.  If anyone knows of a fix, let me know!
