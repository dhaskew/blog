---
layout: post
title: git
sequence: 2
subject: git
summary: git Cheatsheet
---
[Git](https://git-scm.com/) is awesome.

Delete a branch:

```bash
>> git branch -d local_branch_name # only works if the branch is fully merged into origin
>> git branch -D local_branch_name # if "-d" doesn't work, this will force delete
```

Rebase with the branch you forked:

```bash
>> git checkout feature_branch
>> git fetch master
>> git rebase origin/master # replay all your feature_branch changes ontop of the current origin/master
```

Rebase / squash all commits down to 1 commit:

```bash
>> git checkout feature_branch
>> git rebase -i HEAD~3 # start the process of "squash"ing the last 3 commits into 1
```
