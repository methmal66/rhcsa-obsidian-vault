---
tags:
  - question
  - rh124/Ch7_Permissions
reference:
  - "[[Permissions]]"
related:
  - "[[Set permissions to a directory]]"
  - "[[Grant full access to user and group only]]"
---

Allow **davis** to get full access to **john**'s' home directory.

> [!info]- Answer
>
> 1.  `setfacl -mR u:davis:rwx /home/john`
> 2.  `getfacl /home/john` to verify the config
