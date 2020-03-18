# Hackintosh-OptiPlex-9020M
**Only tested on Clover EFI bootloader.**

This is the Hackintosh EFI Folder for Dell OptiPlex 9020 Micro. The configuration settings support MacOS Catalina 10.15.3 with resolution up to 2560 x 1440. My CPU is a Mobile i7 4980HQ modified from FCBGA 1364 to LGA 1150, the EFI should also support other low TDP Haswell CPUs with HD4600. HiPDI support can be actived with [One Key HiDPI](https://github.com/xzhih/one-key-hidpi/blob/master/README.md) script. You will have to **generate a new serial and SmUUID** before login to your iCloud account.

## Hardware Specs
* **Barebone Chassis**: [Dell OptiPlex 9020M](https://www.dell.com/aw/business/p/optiplex-9020m-desktop/pd) with 2 DP Ports
* **CPU**: [Intel® Core™ i7-4980HQ](https://ark.intel.com/products/83503/Intel-Core-i7-4980HQ-Processor-6M-Cache-up-to-4-00-GHz-)
* **iGPU**: Intel® Iris® Pro Graphics 5200
* **RAM**: 16GB DDR3L 1600 Daul Channel 
* **HDD**: Samsung 840 EVO 120GB
* **Wi-Fi & Bluetooth**: BCM94360CS2 with NGFF Adapter

## What Works
* CPU Turbo Boost & Thermal Throttling
* Integrated Graphics with acceleration
* Daul monitor output at 2560 x 1440
* Integrated Audio Output/Input
* All USB Ports
* LAN & Wireless Network
* Airdrop & Airplay
* Sleep & Wakeup

## BIOS Settings
- General → Advanced Boot Options: ***uncheck***
- System Configuration → SATA Operation: ***AHCI***
- Secure Boot → Secure Boot Enable: ***Disabled***
- Virtualization Support → VT for Direct I/O: ***uncheck***

## BIOS Settings via GRUB
* Set Pre-Allocated DVMT to 128M: 
** setup_var 0x263 0x04
* Disable CFG lock: 
** setup_var 0xD9F 0x00
