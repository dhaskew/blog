---
layout: post
title: "KMail and Akonadiserver CPU utilization"
date: 2019-06-18 18:46:57 -0400
categories: kmail akonadi kde
---

KMail was chewing CPU and this seemed to help. May also be useful after kmail/akonadi upgrades.

```bash
$> akonadictl fsck
$> akonadictl vacuum
$> akonadictl fsck
$> akonadictl restart
```

Hope this helps.