---
layout: default
title: Tracking path changes
nav_order: 6
has_children: false
parent: Git
---

# Tracking path changes
Versioning file removes and path changes
```bash
# delete the file from project and stage the removal for commit
$ git rm [file]

# change an existing file path and stage the move
$ git mv [existing-path] [new-path]

# show all commit logs with indication of any paths that moved
$ git log --stat -M
```
