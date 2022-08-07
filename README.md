# Hackintosh configuration for an Asus Z390i using opencore. 

### This is NOT a copy and paste to get it working repository - the folder structure is meant for backup purpose only. Kindly refer to [dortania](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html) to build your own config/USB. If you have similar hardware and are running into issues with the config.plist, feel free to open an issue


![Monterey](https://img.shields.io/badge/macOS-12.5-brightgreen) ![OpenCore](https://img.shields.io/badge/OpenCore-0.8.3-blue)

![Desktop](Images/desktop-12.0.png)

![imessage](Images/imessage-12.0.png)

![WiFi](Images/WiFi-12.0.png)

![xcode](Images/xcode-12.0.png)

![BT](Images/bluetooth-12.0.png)

USB Header Mappings taken from
[simonculton](https://github.com/simoncoulton/opencore-asus-rog-strix-z390i)

![usb](https://github.com/simoncoulton/opencore-asus-rog-strix-z390i/raw/master/usbports.jpeg)

<details>
<summary><strong> Hardware </strong></summary>
<br>

| Category  | Component                            |
| --------- | ------------------------------------ |
| CPU       | [Intel Core i9-9900k](https://ark.intel.com/content/www/us/en/ark/products/186605/intel-core-i9-9900k-processor-16m-cache-up-to-5-00-ghz.html) |
| Mobo      | [Asus Rog Strix Z390-I Gaming](https://rog.asus.com/sg/motherboards/rog-strix/rog-strix-z390-i-gaming-model/)
| SSD       | [Adata XPG SX8200 Pro PCIe Gen3x4 M.2 2280 Solid State Drive](https://www.xpg.com/us/xpg/583) |
| Display   | [Prism Plus X315/C315 Max](https://prismplus.sg/products/prism-c315-max), Anmite 27 inch IPS |
| WiFi & BT | Dell DW1560 |
| GPU       | [Sapphire Pulse 6800XT 16g gddr6](https://www.sapphiretech.com/en/consumer/pulse-radeon-rx-6800-xt-16g-gddr6) |

- This motherboard was specifically selected because it was the only one in stock with a removable WiFi card. The stock WiFi card was removed and replaced with a DW1560.
</details>

<details>


<details>
<summary><strong> Features </strong></summary>
  
| Feature  | Status                            |
| --------- | ------------------------------------ |
 | WiFi | :white_check_mark: |
 | iMessages | :white_check_mark: |
 | USB | :white_check_mark: |
 | Onboard Audio | :white_check_mark: |
 | Dual Screens through RX580 (DP/HDMI output) | :white_check_mark: |
 | Bluetooth | :x: Bluetooth is buggy on MacOS 12. Works sometimes then fucks up and requires a reboot. |
 | Sidecar (Both wired via USB-C <-> iPad Pro and wireless (same wifi network))  | :white_check_mark: |
 | Airdrop | :white_check_mark: |
 | Netflix DRM on Safari | :x:  Refer to [acidanthera](https://github.com/acidanthera/bugtracker/issues/1034) |
 
 
## A note about Sidecar.
For sidecar, you have to ensure that within BIOS, iGPU multi monitor mode is enabled, with a reserved memory of 64mb.

Even though in config.plist the reserved memory is set to 19mb for the iGPU, this will only act as a failover.

Take note to set the primary GPU to auto in BIOS if using a dGPU like I am.

## A note about netflix
Still doesn't work what's new.

I love paying for something that is DRM'ed so heavily I can't even watch the 4k I paid for on linux.

</details>

