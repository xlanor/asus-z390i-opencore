# Hackintosh configuration for an Asus Z390i using opencore. 

![BigSur](https://img.shields.io/badge/macOS-11.4--alpha3-brightgreen) ![OpenCore](https://img.shields.io/badge/OpenCore-0.6.9-blue)


<details>
<summary><strong> HARDWARE </strong></summary>
<br>

| Category  | Component                            |
| --------- | ------------------------------------ |
| CPU       | [Intel Core i9-9900k](https://ark.intel.com/content/www/us/en/ark/products/186605/intel-core-i9-9900k-processor-16m-cache-up-to-5-00-ghz.html) |
| SSD       | [Adata XPG SX8200 Pro PCIe Gen3x4 M.2 2280 Solid State Drive](https://www.xpg.com/us/xpg/583) |
| Display   | [Prism Plus X315/C315 Max](https://prismplus.sg/products/prism-c315-max), Anmite 27 inch IPS |
| WiFi & BT | Dell DW1560 |
| GPU       | [Powercolor Red Devil RX580](https://www.powercolor.com/product?id=1493084304) |

- This motherboard was specifically selected because it was the only one in stock with a removable WiFi card. The stock WiFi card was removed and replaced with a DW1560.
</details>

<details>
<summary><strong> Screenshots </strong></summary>

![Desktop](Images/desktop.png)
![imessage](Images/imessage.png)
![WiFi](Images/WiFi.png)

USB Header Mappings taken from
[simonculton](https://github.com/simoncoulton/opencore-asus-rog-strix-z390i)

![usb](https://github.com/simoncoulton/opencore-asus-rog-strix-z390i/raw/master/usbports.jpeg)
</details>

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
