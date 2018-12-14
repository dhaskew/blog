---
layout: post
title: Installation
sequence: 2
subject: Installation 
summary: Details related to the installation of Manjaro Linux
---

Installation went fine, with the exception of wireless.  I don't remmeber the details, but I mention it so that if you already have Linux on it (mine came with Ubuntu) .. then take a few minutes to learn about your wireless hardware and its configuration before attempting to install Manjaro. 


Also, getting the EFI bootloader working as expected was a new experience for me, but seemed to go ok

efibootmgr controls the efi menu (F12 Menu)

[Install Help - Bootloader / Grub - Newbie Corner - Manjaro Linux Forum](https://forum.manjaro.org/t/install-help-bootloader-grub/50053)

``` bash
$> efibootmgr 
BootCurrent: 0009
Timeout: 0 seconds
BootOrder: 0009,0002,0003,0004,0005
Boot0002* Diskette Drive
Boot0003* M.2 PCIe SSD
Boot0004* USB Storage Device
Boot0005* CD/DVD/CD-RW Drive
Boot0007* UEFI: THNSN5512GPUK NVMe TOSHIBA 512GB, Partition 1
Boot0009* manjaro
```
