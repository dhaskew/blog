---
layout: post
title: Console Fonts
sequence: 4
subject: Console Fonts
summary: How to make console fonts better/bigger.
---

Fonts on the framebuffer console where too small post install, both on the VTs and the boot-up and shutdown outputs.  I set out to make some of them bigger.

```bash

$> ls -l /usr/share/kbd/consolefonts/ #show available fonts

$> showconsolefont # might be useful to look at this output before and after changes?

$> setfont ter-132b # set the font temporarily for that session

$> cat /etc/vconsole.conf # makes permanent?
KEYMAP=us
FONT=ter-132b
FONT_MAP=
```

Even after pdating vconsole.conf, some small, unreadable fonts remain. Some small fonts persist on early boot.  May need tweaking.

I tried updating the HOOKS setting of initcpio, to add CONSOLEFONT but it didn't seem into impact anything.  I suspect my machine is booting too fast to matter.

further reading: [https://wiki.archlinux.org/index.php/Mkinitcpio#HOOKS]()

```bash
$> cat /etc/mkinitcpio.conf | grep ^HOOKS
HOOKS="base udev autodetect modconf block keyboard keymap resume filesystems fsck consolefont"

$> mkinitcpio -P # apply config changes
```

Potentially UsefulLinks:

[https://wiki.manjaro.org/index.php?title=Make_GRUB_menu_%26_boot-up/down_fonts_bigger]()

[https://wiki.archlinux.org/index.php/Linux_console#Fonts]()

[https://wiki.archlinux.org/index.php/Kernel_mode_setting#Early_KMS_start]()
