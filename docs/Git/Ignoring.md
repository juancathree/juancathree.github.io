---
layout: default
title: Ignoring patterns
nav_order: 7
has_children: false
parent: Git
---

# Ignoring patterns
Preventing unintentional staging or commiting of files
```bash
# Save a file with desired paterns as .gitignore with either direct string matches or wildcard globs.
logs/
*.notes
pattern*/

# system wide ignore patern for all local repositories
$ git config --global core.excludesfile [file]
```
