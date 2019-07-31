---
layout: post
title: Intel
sequence: 11
subject: Intel
summary: Video card info
---

Enable guc/huc

```bash
$> cat /etc/modprobe.d/i915.conf 
options i915 enable_guc=2
```

Then reboot

Verify the settings took:

```bash
$> sudo dmesg | grep -i huc
[    2.989384] [drm] HuC: Loaded firmware i915/kbl_huc_ver02_00_1810.bin (version 2.0)
[    3.011484] i915 0000:00:02.0: HuC enabled
```

```bash
$> sudo dmesg | grep -i guc
[    2.950760] Setting dangerous option enable_guc - tainting kernel
[    3.001028] [drm] GuC: Loaded firmware i915/kbl_guc_ver9_39.bin (version 9.39)
[    3.011480] i915 0000:00:02.0: GuC firmware version 9.39
[    3.011482] i915 0000:00:02.0: GuC submission disabled
```

```bash
$> sudo cat /sys/kernel/debug/dri/0/i915_huc_load_status
HuC firmware: i915/kbl_huc_ver02_00_1810.bin
        status: fetch SUCCESS, load SUCCESS
        version: wanted 2.0, found 2.0
        header: offset 0, size 128
        uCode: offset 128, size 218304
        RSA: offset 218432, size 256

HuC status 0x00006080:
```


```bash
$ sudo cat /sys/kernel/debug/dri/0/i915_guc_load_status
GuC firmware: i915/kbl_guc_ver9_39.bin
        status: fetch SUCCESS, load SUCCESS
        version: wanted 9.39, found 9.39
        header: offset 0, size 128
        uCode: offset 128, size 147392
        RSA: offset 147520, size 256

GuC status 0x800300ec:
        Bootrom status = 0x76
        uKernel status = 0x0
        MIA Core status = 0x3

Scratch registers:
         0:     0xf0000000
         1:     0x15c540
         2:     0x0
         3:     0x5f5e100
         4:     0x0
         5:     0x109fd3
         6:     0x0
         7:     0x8
         8:     0x11
         9:     0x8e240
        10:     0x0
        11:     0x0
        12:     0x0
        13:     0x0
        14:     0x0
        15:     0x700000

```


Useful Links:

<https://wiki.archlinux.org/index.php/Intel_graphics>

<https://wiki.gentoo.org/wiki/Intel#Feature_support>

<https://wiki.archlinux.org/index.php/Dell_XPS_13_(9360)>

<https://ubuntuforums.org/showthread.php?t=2356657>

<https://wiki.archlinux.org/index.php/Hardware_video_acceleration>

