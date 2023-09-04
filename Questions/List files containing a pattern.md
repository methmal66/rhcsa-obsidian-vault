---
tags:
  - question
  - rh124/Ch3_File-basics
related:
  - "[[Copy lines containing a pattern]]"
  - "[[Find and copy files]]"
---

Find All Files in **/etc** (not subdirectories) that contain text **"chrony"** (ignore case).

> [!info]- Answer
>
> 1.  `grep -d skip -il chrony /etc/*`
