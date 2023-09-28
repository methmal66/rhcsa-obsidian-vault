---
tags:
  - question
  - rh134/Ch7_NetStorage
references:
  - "[[Network File Sharing]]"
---
Some users home directory is shared from your system. Using showmount -e localhost command, the shared directory is not shown. Make access the shared users home directory

> [!faq]- Answer
> 1. Verify if the directory exist. `ls -ld /home`
> 2. Verify if the directory is being shared. `cat /etc/exports`
> 3. Verify if the nfs-server is running. `systemctl status nfs-server`
