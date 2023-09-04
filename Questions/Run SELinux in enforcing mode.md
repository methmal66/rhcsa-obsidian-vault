---
tags:
  - question
  - rh134/Ch4_SELinux
reference:
  - "[[Enforcement mode]]"
---

SELinux must be running in the enforcing mode

> [!faq]- Answer
>
> 1.  `setenforce 1` to set mode temporary
> 2.  `getenforce` to check
> 3.  `vim /etc/selinux/config` then change the line into `selinux=enforcing`, to set mode permanently
