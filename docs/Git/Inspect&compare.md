---
layout: default
title: Inspect & compare
nav_order: 5
has_children: false
parent: Git
---

# Inspect & compare
Examining logs, diffs and object information
```bash
# show the commit history for the currently active branch
$ git log

# show the commits on branchA that are not on branchB
$ git log branchB..branchA

# show the commits that changed file, even across renames
$ git log --follow [file]

# show the diff of what is in branchA that is not in branchB
$ git diff branchB...branchA

# show any object in Git in human-readable format
$ git show [SHA]
```
