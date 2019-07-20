---
layout: post
title: Backlight
sequence: 10
subject: Backlight
summary:  How to manipulate the backlight
---

Create the following file (`/etc/udev/rules.d/backlight.rules`) and reboot:

```bash
>$ cat /etc/udev/rules.d/backlight.rules 

ACTION=="add", SUBSYSTEM=="backlight", KERNEL=="intel_backlight", RUN+="/bin/chgrp video /sys/class/backlight/%k/brightness"
ACTION=="add", SUBSYSTEM=="backlight", KERNEL=="intel_backlight", RUN+="/bin/chmod g+w /sys/class/backlight/%k/brightness"
```

Note, if you don't create the file `/etc/udev/rules.d/backlight.rules` file then you will need to execute the commands as root.

As a member of the video group .... it will allow you to do the following:

```bash

>$ cat /sys/class/backlight/intel_backlight/actual_brightness 
3000

>$ cat /sys/class/backlight/intel_backlight/max_brightness 
7500

>$ echo 4000 > /sys/class/backlight/intel_backlight/brightness 
```

also see the [arch backlight guide](https://wiki.archlinux.org/index.php/Backlight)

also see the [arch udev guide](https://wiki.archlinux.org/index.php/Udev#udev_rule_example)

