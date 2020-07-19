---
layout: post
title: 1Password
sequence: 9
subject: 1Password
summary: 1Password CLI Details
---

I use the 1Password CLI to automate alot of my email setup and other stuff.

Useful Links:

* <https://support.1password.com/command-line-getting-started/>

* <https://support.1password.com/command-line/>

* <https://support.1password.com/sign-in-troubleshooting/#if-youre-asked-for-a-sign-in-address>


Useful Commands:
```bash
op signin my.1password.com user@email.com

eval $(op signin)  #sets an env variable that contains a session token #good for 30 mins

eval $(echo VAULT_PWD_GOES_HERE | op signin)  # could run this to avoid the password prompt in a script


op list items

op get item offlineimap-secret-item-name --fields Passwords
```
