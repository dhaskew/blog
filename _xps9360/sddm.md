---
layout: post
title: SDDM
sequence: 5
subject: SDDM
summary: How to make login manager better.
---

The SDDM login manager and its various widgets and fonts looked too small on the UHD screen while in native resolution.

So I uppedd the DPI setting by:

```bash
# https://wiki.archlinux.org/index.php/SDDM

[dhaskew@xps13 ~]$ cat /etc/sddm.conf | grep ServerArguments
ServerArguments=-nolisten tcp -dpi 184 
```

Adding the "dpi" option made a world of difference.