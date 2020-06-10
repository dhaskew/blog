---
layout: post
title: goobook 
sequence: 8
subject: goobook 
summary: goobook is a google contacts cli client 
---

I use [goobook](https://gitlab.com/goobook/goobook) to work with google contacts on the command line.

Useful Info: 

* <https://pypi.org/project/goobook/>
* <https://gitlab.com/goobook/goobook/-/issues/83>

Notes:

* setup was annoying to figure out 
  * <https://console.developers.google.com>
  * create a project
  * enable some APIs
    * contacts / people ?
  * oauth consent screen
    * create one
    * update with scopes?
  * create credentials
    * OAUTH 2.0 Client IDs
    * web type
    * redirect uri http://localhost:8080
    * download as .goobook_client_secret.json


```bash
>> goobook authenticate  # will open default browser and start workflow
>> goobook query <NAME>
>> goobook dquery <NAME> # prints more info than query
```
