# Modern Hackintosh Guide - My Experience and Notes

Using OpenCore-0.5.9-RELEASE with Catalina

This is a debug version to help folks find issues while building a Hackintosh!

| Component     | Type                                              |
|---------------|---------------------------------------------------|
| SMBIOS Model | iMacPro1,1                                         |
| Motherboard  | ASUS TUF X570 Plus     BIOS Version 2407           |
| CPU          | AMD Ryzen 3900X                                    |
| GPU          | AMD XFX RX550      Flashed to with Sapphire ROM!   |
| RAM          | 64Gb                                               |
| WiFi / BT    | N/A                                                |
| Ethernet     | Realtek® L8200A                                    |

This should be about to boot into the Mac Installer


## ASUS BIOS Version:2407

(Upgrading ASUS Firmware to 2407 - ** you need to update the Booter settings)


### BIOS Settings

Bios Settings these are some of the settings, I changed.  

### Disable:

* Fast Boot (Important)
* CSM  (Important)
* IOMMU
* AMT Native NVMe Driver Support
* USB power delivery in Soft Off State (S5) 
* fTPM NV for factory reset 

### Enable:

* Power On BY PCI-E
* PCIE16_1 Mode  GEN 3


## XFX RX580
XFX RX580 Issue (See XFX folder in this REPO)
Roms are included - USE AT YOUR OWN RISK!!
https://www.insanelymac.com/forum/topic/338516-opencore-discussion/?page=91


## Kext's

- AGPMInjector.kext - for GPU power management
- AMD-USB-Map.kext - Mapping USB port 
- AmdCPUMonitor.kext
- AppleALC.kext - Audio
- FakeSMC.kext - Driver for emulation SMC device with hardware sensors support
- Lilu.kext
- NullCPUPowerManagement.kext - 
- RadeonMonitor.kext
- RealtekRTL8111.kext- Network Card
- VirtualSMC.kext 
- W836x.kext - W836x for chips Winbond/Nuvoton 83xxx on ASUS motherboards (LPC chip sensors, motherboard parameters like FAM, Voltages, temperatures)
- WhateverGreen.kext 


### Need to add

- AMDRyzenCPUPowerManagement.kext - AMD Power Gadget.
- SMCAMDProcessor.kext  - (After AMDRyzenCPUPowerManagement)

Orignal Text from COKelly


## DISCLAIMER

This is a guide for Windows 10 based systems. I am not responsible for any damage caused to your components, data loss, or anything else that may happen throughout this process. Follow this guide at your own risk! The steps listed below worked for my components. You will find my components listed under the [My Build Components](#my-build-components) section. There is no guarantee this guide will work for your components. You are responsible for reading about and knowing the guides, documentation, and programs listed below. You may need to download additional programs and seek other resources than what is listed. The steps within this guide are for AMD based components, however there are links within [Resources](#resources) that have steps for Intel and NVIDIA based components. Without further ado, good luck and ask questions!


## Resources

Reddit: https://www.reddit.com/r/hackintosh/

AMD OSX Forum: https://forum.amd-osx.com/

AMD Vanilla Install Guide: https://vanilla.amd-osx.com/

gibMacOS: https://github.com/corpnewt/gibMacOS

OpenCore: https://github.com/acidanthera/OpenCorePkg/releases

OpenCore Vanilla Guide: https://khronokernel-2.gitbook.io/opencore-vanilla-desktop-guide/

KEXTs: https://onedrive.live.com/?cid=fe4038da929bfb23&id=FE4038DA929BFB23%21455036&authkey=%21APjCyRpzoAKp4xs

## Credit

* Reddit
  * r/SlackyHacky
  * r/dj_chapz
  * r/Shaneee92
  * r/johnklos
* AMD-OSX Forum
  * QuickTime
  * fozteh
  * Brass Ensemble
  * Villegasdv
  * pulsar7377
* Other
  * Every link within [Resources](#resources), without your tools and guides this would not be possible!

## My Build Components

| Component     | Type                             |
|---------------|----------------------------------|
| SMBIOS Model | iMacPro1,1                        |
| Motherboard  | ASUS TUF X570 Plus     BIOS Version 2407!          |
| CPU          | AMD Ryzen 3900X                |
| GPU          | AMD XFX RX550      Flashed to with Sapphire ROM!    |
| RAM          | 64Gb |
| WiFi / BT    | N/A                               |
| Ethernet     | Realtek® L8200A                   |


## Benchmarks

* Current Benchmarks at the time are as follows: (Note: these have not been optimized to their fullest potential)
  * Geekbench 5.0.4
    * Single-Core: ~1215
    * Multi-Core Score: ~12436

  * Geekbench 4.4.2
    * Single-Core: ~5618
    * Multi-Core Score: ~55628

  


