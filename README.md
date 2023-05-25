# EFI-X270
EFI works fine for X270 I5 7200U, Opencore(0.9.2) and Mojave(10.14.6)

# Hardware
 * Intel(R) Core(TM) i5-7200U CPU @ 2.50GHz
 * Intel HD Graphics 620 
 * Mobile 7th Generation Intel(R) Processor Family I/O LPC Controller (U Premium) - 9D58
 * Synaptics HID-Compliant Touch pad Device
 * Intel Kaby Lake HDMI @ Intel Sunrise Point-LP PCH - High Definition Audio Controller [C1] PCI
 * Realtek ALC298 @ Intel Sunrise Point-LP PCH - High Definition Audio Controller [C1] PCI
 * Intel Dual Band Wireless-AC 8265 WiFi Adapter PCI
 * Intel Ethernet Connection (4) I219-V PCI
 * SAMSUNG MZVLW256HEHP-000L7
 
 # What's works
* Power Management
* Audio Output&Input
* USB Ports
* WiFi
* Bluetooth
* Ethernet
* Docking USB Ports
* Docking Ethernet
* HDMI Out
* TouchPad (Click and gestures)
* TrackPoint
* Sleep

Note: Bluetooth soundbar/mouse work, but bluetooth keyboard not work until upgraded to Monterey.
 
 # Upgrade
 1. to Catalina(10.15.7) and Big Sur(11.7.7), works fine, what you need is to replace the correct version of Airportitlwm.
 2. to Monterey(12.6.5), also replace the correct version of Airportitlwm., bluetooth and secureboot need update and configure, I test working well.
 
 Note: 
 
# Other information
for audio, I checked the 298, supports below codec, and I test some , 3 and 22 are working, 11, 13, 16, 21 are not working, others have not tested.

```0x100101, 0x100103, layout 3, 11, 13, 16, 21, 22, 28, 29, 30, 32, 33, 47, 66, 72, 99```

# Issues
* the HDMI has some strange issues. when it wake up, macOS is unable to find the output unless you pull out and plug in again the HDMI cable.
---solved, with add "igfxonln=1" in boot arg in Nvram.
