---
layout: post
title:  "Systemd Notes"
date:   2019-11-07 18:46:57 -0400
categories: linux systemd
---

How long did the last startup take?


```bash
$ systemd-analyze 
Startup finished in 7.329s (firmware) + 5.115s (loader) + 1.682s (kernel) + 2.403s (userspace) = 16.530s 
graphical.target reached after 1.833s in userspace
```

List services enabled at startup:

```bash
$ systemctl list-unit-files | grep enabled
```

If you need to know which services take the longest to startup:

```bash
$ systemd-analyze blame
           565ms systemd-timesyncd.service
           564ms lvm2-monitor.service
           561ms tlp.service
           510ms dev-nvme0n1p2.device
           457ms upower.service
           391ms systemd-logind.service
           260ms systemd-udevd.service
           192ms systemd-journald.service
           192ms ldconfig.service
           165ms ModemManager.service
           108ms udisks2.service
           ...
           ...
```

If you want to disable/enable a service:

```bash
sudo systemctl disable SERVICE_NAME
sudo systemctl enable SERVICE_NAME
```