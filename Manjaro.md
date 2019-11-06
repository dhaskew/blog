---
layout: page
title: Manjaro
permalink: /manjaro/
---

A collection of [Manjaro](http://www.manjaro.org) / [Arch](https://www.archlinux.org/) related notes that don't have a home of their own yet.

Restart the network

```bash
systemctl restart NetworkManager
```

Toggle the wifi radio off/on with **nmcli**
```bash
$ nmcli radio wifi off
$ nmcli radio wifi on
```