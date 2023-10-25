# Fully Functional MSI MPG B550 Gaming Plus Hackintosh

![Screenshot 2023-10-25 at 00 58 52-3](https://github.com/CCSilvs/EFI-MSI-MPG-B550-GAMING-PLUS/assets/91890693/d275c2fe-6124-4996-b5fc-f6cfbae9bb99)


**MacOS version:** Ventura 13.6
<br>
**OpenCore version:** 0.9.5

## **Specs**
| **Component** | **Model** |
| ------------- | --------- |
| CPU | AMD Ryzen 7 3700X |
| Motherboard | MSI MPG B550 Gaming Plus |
| GPU | ASUS DUAL AMD RADEON RX 5600 XT EVO, 6GB GDDR6 |
| RAM | 16GB XPG Gammix D10 3200MHz CL16 (2x8GB) |
| WAN | Fenvi T919 1750Mbps (BCM94360CD) |
| LAN CHIPSET | Realtek® RTL8111H Gigabit LAN |
| AUDIO CHIPSET | Realtek® ALC892/ALC897 Codec |
| STORAGE | 1TB Adata XPG SX8200 PCIe 3.0 3500/300MB/s (r/w) |
| PARTITIONING | 512GB APFS MacOS + 512GB NTFS Windows 11 |
| CPU Cooler | MasterAir MA410M TUF Gaming Edition |
| PSU | EVGA600B 600W, 80 Plus Bronze |
| CASE | XPG Cruiser, Mid-Tower |
| COOLING | 2x3 fan kits by XPG & Coolermaster |
| SCREEN 1 | Horizontal: LG 29UM69G - 29" Ultrawide (2560x1080px) | 
| SCREEN 2 | Vertical: Ozone OZDSP28IPS - 28" Standard (3840x2160px) |

## **What works**
- All MacOS since Big Sur to Ventura (Sonoma in the next Opencore update)
- Audio: front panel, rear panel + wifi receivers and speakers
- All USB ports
- Wifi, Bluetooth, Airdrop, Airplay (even with Samsung TV screens), Sidecar
- Everything from iCloud and Apple phones, pads & gadgets
- Temperature monitoring for everything includes GPU
- Sleep/wake up

## **What doesn't work**
- Microphone and line in on rear panel (know AMD issue)
- Optical Digital out

## ACPI used:
- SSDT-CPUR.aml (mandatory for B550 chipset)
- SSDT-EC-USBX-DESKTOP.aml (prebuild)
  
## Opencore Drivers:
- AudioDxe.efi
- HfsPlus.efi
- OpenCanopy.efi
- OpenRuntime.efi
- ResetNvramEntry.efi
- ToggleSipEntry.efi

## Kexts used:
- AGPMInjector.kext (kext to increase Radeon 5000 series performance)
- AMDRyzenCPUPowerManagement.kext
- AppleALC.kext
- AppleMCEReporterDisabler.kext
- FeatureUnlock.kext
- HibernationFixup.kext
- Lilu.kext
- NVMeFix.kext
- RadeonSensor.kext
- RealtekRTL8111.kext
- RestrictEvents.kext
- SMCAMDProcessor.kext
- SMCRadeonGPU.kext
- VirtualSMC.kext
- WhateverGreen.kext

## BIOS Settings

**Disable**
- Fast Boot
- Secure Boot
- Serial/COM Port
- Compatibility Support Module (CSM)

**Enable**
- Above 4G decoding
- Resizable BAR can be set "Auto" or "Enabled", this config.plist already has a setting to mantaing this option enabled to guarantee the best graphical performance in Windows
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- SATA Mode: AHCI

## Geekbench results
CPU <br>
<img width="854" alt="Screenshot 2023-10-25 at 03 23 13" src="https://github.com/CCSilvs/EFI-MSI-MPG-B550-GAMING-PLUS/assets/91890693/a86a2185-6717-4cc6-acfe-1e47fc6dee64">

GPU <br>
<img width="852" alt="Screenshot 2023-10-25 at 03 28 54" src="https://github.com/CCSilvs/EFI-MSI-MPG-B550-GAMING-PLUS/assets/91890693/155cbf58-ee01-4822-a15e-4b468c3b4553">


## Credits
- <p>Special thnx to <a href="https://github.com/luchina-gabriel/"> Gabriel Luchina</a></p>
- <p>His knowledge and repository <a href="https://github.com/luchina-gabriel/BASE-EFI-AMD-RYZEN-THREADRIPPER/"> BASE-EFI-AMD-RYZEN-THREADRIPPER</a></p>

- [Opencore Team](https://dortania.github.io/getting-started/)
