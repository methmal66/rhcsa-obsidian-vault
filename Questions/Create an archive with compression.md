---
tags:
  - question
  - rh124/Ch12_Archives
reference:
  - "[[Archiving]]"
  - "[[Compression]]"
---

Create a backup file named **/root/backup.tar.bz2**, contains the content of **/usr/local**, tar must use bzip2 to compress.

> [!info]- Answer
>
> 1.  `tar -jvcf /root/backup.tar.bz2 /usr/local`
