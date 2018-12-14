---
layout: post
title:  "Using a Superdrive in Linux"
date:   2018-12-13 23:46:57 -0500
categories: linux superdrive udev 
---

You have to send a "magic packet" in order for the drive to work. Really Apple!!!???

```bash

$> ls /dev # list devices

# the drive should be listed as sr0 or sr1

# send the magic packet replace sr0 with your drive
$> sg_raw /dev/sr0 EA 00 00 00 00 00 01

# custom udev rule send magic packet when drive is plugged in
$> cat /etc/udev/rules.d/99-local.rules

ACTION=="add", ATTRS{idProduct}=="1500", ATTRS{idVendor}=="05ac", DRIVERS=="usb", RUN+="/usr/bin/sg_raw /dev/$kernel EA 00 00 00 00 00 01"
```