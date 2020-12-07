# Hackintosh configuration for an Asus Z390i using opencore. 

As backup, because I went and nuked all my previous stuff which is why I switched entirely to opencore.

System specifications:

Asus ROG Strix Z390i ( Wifi Card has been replaced with DW1560 BCM94352Z )

Intel i9-9900k

Powercolor RX580 Red Devil 8GB.

![Desktop](Images/desktop.png)
![imessage](Images/imessage.png)
![WiFi](Images/WiFi.png)

USB Header Mappings taken from
[simonculton](https://github.com/simoncoulton/opencore-asus-rog-strix-z390i)

![usb](https://github.com/simoncoulton/opencore-asus-rog-strix-z390i/raw/master/usbports.jpeg)


What's Working:
- WiFi
- iMessages
- USB
- Onboard Audio
- Dual Screens through RX580 (DP/HDMI output)
- Bluetooth
- Sidecar (Both wired via USB-C <-> iPad Pro and wireless (same wifi network)) 
- Airdrop

What's not working:
- Netflix DRM on Safari (I suspect amazon prime too, even with shiki value set.) This means you will be capped to 720p. Refer to [acidanthera](https://github.com/acidanthera/bugtracker/issues/1034), but the root cause appears to be Lilu userspace being broken. This doesn't affect me because I primarily use other sources to get my TV shows, but it should be a considering factor in whether Big Sur or Catalina is more suitable for you

## A note about Sidecar.
For sidecar, you have to ensure that within BIOS, iGPU multi monitor mode is enabled, with a reserved memory of 64mb.

Even though in config.plist the reserved memory is set to 19mb for the iGPU, this will only act as a failover.

Take note to set the primary GPU to auto in BIOS if using a dGPU like I am.
