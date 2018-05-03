---
layout: post
title: "Find - xargs - grep"
author: R.Boman
tags:
  - bash
---

# How to grep a string from a series of files with spaces in their names?

Wrong way:
```
find . -type f | xargs grep string
```
Better way:
```
find . -type f -print0 | xargs -0 grep string
```
