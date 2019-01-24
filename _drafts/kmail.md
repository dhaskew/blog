
---
layout: post
title: KMail and Akonadiserver CPU utilization
date: 2019-01-01 18:46:57 -0400
---


KMail was chewing CPU and this seemed to help. May also be useful after kmail/akonadi upgrades

```bash
$> akonadictl fsck
$> akonadictl vacuum
$> akonadictl fsck
$> akonadictl restart
```