---
layout: post
title: "Color Man Pages in Terminal"
date: 2019-06-26 15:46:57 -0400
categories: linux bash
---

I found the following online somewhere while trying to get some color / better output when viewing man pages in the terminal.

```bash
export LESS_TERMCAP_mb=$'\E[1;31m'     # begin bold
export LESS_TERMCAP_md=$'\E[1;36m'     # begin blink
export LESS_TERMCAP_me=$'\E[0m'        # reset bold/blink
export LESS_TERMCAP_so=$'\E[01;44;33m' # begin reverse video
export LESS_TERMCAP_se=$'\E[0m'        # reset reverse video
export LESS_TERMCAP_us=$'\E[1;32m'     # begin underline
export LESS_TERMCAP_ue=$'\E[0m'        # reset underline
export GROFF_NO_SGR=1                  # for konsole and gnome-terminal
```

I've saved it to `~/.bash_termcap` and added the following to `~/.bashrc` : 

```bash
if [ -f ~/.bash_termcap ]; then
        source ~/.bash_termcap
fi
```