---
hide:
  - navigation
  - toc
---

# Hardware

HP EliteDesk 
---

HP EliteDesk 705 G4 DM 65W

| Specs |  |
| --- | --- |
CPU: | AMD Ryzen 5 PRO 2400G
RAM: | 32 GiB SODIMM DDR4 2400 MHz

| Storage| |
| --- | --- |
sda (boot): | Western Digital WDS500G2B0A 500GB
sdb | 256GB Flash Drive for [OMV](../Services/OMV.md)
sdc | Unused Port - HDD Failed
sdd | 256GB SSD, mounted at /mnt/ssd <br> Additional Proxmox Storage <br> Mounted in hard drive enclosure *See below* 
sde | 12 TB HDD, mounted at /mnt/hard-12tb <br> Passed through to [Jellyfin](../Services/Jellyfin.md) <br> Mounted in hard drive enclosure *See below*

---

Raspberry Pi 4 Model B
---

Running OpenWRT to setup a private LAN, no matter the internet source. <br>
See [Networking](../Networking/index.md) for more information.

---

TP-Link 5-Port Gigabit Unmanaged Ethernet Switch
---

TL-SG705 <br>
Allows for extended ethernet ports.

---

TP-Link Router
---

Roam 6 AX1500 Portable Wi-Fi 6 Travel Router <br>
Creates a high speed access point to the LAN. <br><br>
SSID: Keep it on the Download <br>
Password: *See [Vaultwarden](../Services/Vaultwarden.md)*

---

CENMATE Hard Drive Enclosure
---

Aluminum 2 Bay Hard Drive Enclosure <br>
USB A - DAS <br>
Allows for storage expansion <br>
<br>
Currently mounted:

- /dev/sdd
- /dev/sde