---
layout: default
title: Branch & merge
nav_order: 4
has_children: false
parent: Git
---

# Branch & merge
solating work in branches, changing context, and integrating changes
```bash
# list your branches. a * will appear next to the currently active branch
$ git branch

# create a new branch at the current commit
$ git branch [branch-name]

# switch to another branch and check it out into your working directory
$ git checkout [branch-name]

# merge the specified branch’s history into the current one
$ git merge [branch]
```
