---
layout: post
title:  "Spotify, HiDPI and You"
date:   2018-12-14 10:00:57 -0500
categories: linux superdrive udev 
---

If you have a [xps9360]({{ site.baseurl }}/xps9360/) like I do, then your beautiful UHD screen is wonderful.  What's not wonderful is how some applications don't place nice.  If you have problems with Spotify being unreadble .... try this:

```bash
$> spotify --force-device-scale-factor=1.5
```

<https://community.spotify.com/t5/Desktop-Linux-Windows-Web-Player/Linux-client-barely-usable-on-HiDPI-displays/td-p/1067272>