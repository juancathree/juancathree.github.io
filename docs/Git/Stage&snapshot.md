---
layout: default
title: Stage & snapshot
nav_order: 3
has_children: false
parent: Git
---

# Stage & snapshot
Working with snapshots and the Git staging area

```bash
# show modified files in working directory, staged for your next commit
$ git status

# add a file as it looks now to your next commit (stage)
$ git add [file]

# unstage a file while retaining the changes in working directory
$ git reset [file]

# diff of what is changed but not staged
$ git diff

# diff of what is staged but not yet commited
$ git diff --staged

# commit your staged content as a new commit snapshot
$ git commit -m “[descriptive message]”
```
