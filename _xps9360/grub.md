---
layout: post
title: Grub
sequence: 3
subject: Grub
summary: Things you might want to know about the bootloader.
---

The QHD screen on the XPS 9360 is beautiful, but fonts are an issue in some cases because of HiDPI support in Linux being kinda fragmented.  I had to make the grub font much larger to make grub usable.  

Here's what I did:

```bash
#prepare a font to be used by grub
$> sudo grub-mkfont --output=/boot/grub/fonts/DejaVuSansMono20.pf2 --size=20 /usr/share/fonts/TTF/DejaVuSansMono.ttf

#Edit grub's config so that it references the newly created font

$> cat /etc/default/grub | grep GRUB_FONT
GRUB_FONT=/boot/grub/fonts/DejaVuSansMono20.pf2

#This will make grub reload its config file(s)
$> sudo update-grub
```

Other potentially useful info:

[https://wiki.manjaro.org/index.php?title=Make_GRUB_menu_%26_boot-up/down_fonts_bigger]()
