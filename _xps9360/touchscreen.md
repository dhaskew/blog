---
layout: post
title: Touchscreen
sequence: 7
subject: Touchscreen
summary: How to enable/disable the touchscreen.
---

The touchscreen worked well out of the box. So well in fact, I use it way more than I thought I would.  So what's wrong with that?  Well, if you touch your screen all the time, then you have to clean it pretty regularly to keep the smudges in check.  How do you clean a touchscreen without random clicking stuff and making a mess?  


```bash
$> xinput # get <ID> of touchscreen
$> xinput disable <ID>
$> xinput enable <ID>
```
