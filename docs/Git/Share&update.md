---
layout: default
title: Share & update
nav_order: 8
has_children: false
parent: Git
---

# Share & update
Retrieving updates from another repository and updating local repos
```bash
# add a git URL as an alias
$ git remote add [alias] [url]

# fetch down all the branches from that Git remote
$ git fetch [alias]

# merge a remote branch into your current branch to bring it up to date
$ git merge [alias]/[branch]

# Transmit local branch commits to the remote repository branch
$ git push [alias] [branch]

# fetch and merge any commits from the tracking remote branch
$ git pull
```
