---
layout: post
title:  "Linux Hardware Info"
date:   2018-11-16 00:00:00 -0400
categories: linux desktop hardware
---

{% highlight bash %}
=> inxi -Fxxxz
{% endhighlight %}

Show info about memory hardware:

```bash
$ sudo lshw -c memory     
  *-firmware                
       description: BIOS
       vendor: Dell Inc.
       physical id: 0
       version: 1.3.2
       date: 01/18/2017
       size: 64KiB
       capacity: 15MiB
       capabilities: pci pnp upgrade shadowing cdboot bootselect edd int13floppynec int13floppy1200 int13floppy720 int13floppy2880 int5printscreen int9keyboard int14serial int17printer acpi usb smartbattery biosbootspecification netboot uefi
  *-memory
       description: System Memory
       physical id: 38
       slot: System board or motherboard
       size: 16GiB
     *-bank:0
          description: Row of chips LPDDR3 Synchronous Unbuffered (Unregistered) 1867 MHz (0.5 ns)
          product: MT52L1G32D4PG-107
          vendor: Micron
          physical id: 0
          serial: 00000000
          slot: System Board Memory
          size: 8GiB
          width: 64 bits
          clock: 1867MHz (0.5ns)
     *-bank:1
          description: Row of chips LPDDR3 Synchronous Unbuffered (Unregistered) 1867 MHz (0.5 ns)
          product: MT52L1G32D4PG-107
          vendor: Micron
          physical id: 1
          serial: 00000000
          slot: System Board Memory
          size: 8GiB
          width: 64 bits
          clock: 1867MHz (0.5ns)
  *-cache:0
       description: L1 cache
       physical id: 3c
       slot: L1 Cache
       size: 128KiB
       capacity: 128KiB
       capabilities: synchronous internal write-back unified
       configuration: level=1
  *-cache:1
       description: L2 cache
       physical id: 3d
       slot: L2 Cache
       size: 512KiB
       capacity: 512KiB
       capabilities: synchronous internal write-back unified
       configuration: level=2
  *-cache:2
       description: L3 cache
       physical id: 3e
       slot: L3 Cache
       size: 4MiB
       capacity: 4MiB
       capabilities: synchronous internal write-back unified
       configuration: level=3
  *-memory UNCLAIMED
       description: Memory controller
       product: Sunrise Point-LP PMC
       vendor: Intel Corporation
       physical id: 1f.2
       bus info: pci@0000:00:1f.2
       version: 21
       width: 32 bits
       clock: 33MHz (30.3ns)
       configuration: latency=0
       resources: memory:dc32c000-dc32ffff
```
