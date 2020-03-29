---
layout: post
title: Vim
sequence: 1
subject: Vim
summary: Vim Cheatsheet
---

[Vim](https://www.vim.org) is awesome.

```vimscript
:edit <filename> # edit a file
:vsplit # virtical split
:bd # buffer delete
```

Resizing Splits:

https://vim.fandom.com/wiki/Resize_splits_more_quickly

```vimscript
:resize 60 # resize virtical rows to 60
:vertical resize 80 # resize a vertical split to 80 columns
:vertical resize +5 # add 5 columns to the width
```

Folding:

```vimscript
:set foldenable           # enable folding
:set foldmethod = indent  # folds determined by indent level
:set nofoldenable         # disable folding
```

Folding key combos:

```vimscript
zM # close all folds
zR # open all folds
zc # close current fold the cursor is in
zo # open current fold the cursor is in
za # toggle the current fold the cursor is in

zA # toggle the current fold (and any sub-folds) the curson is in
zO # open the fold and its decendant folds
zC # close the fold and its ancestors
```

Moving about the history:

```vimscript
:jumps # prints jump list
Ctrl-I # jump to the next newest jump location in the jump list
Ctrl-O # jump to the next oldest jump location in the jump list
<num> Ctrl-I # jump to the <num> newest location in the jump list
<num> Ctrl-O # jump to the <num> oldest location in the jump list
```


