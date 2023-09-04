---
tags:
  - question
  - rhcsa/rh124/Ch7_Permissions
reference:
  - "[[Permissions]]"
related:
  - "[[Set permissions to a directory]]"
  - "[[Allow access to others home directory]]"
---
Make **/data** directory so that only the user owner and group owner member can fully access.

>[!info]- Answer
>1. `chmod 770 /data`
>2. `ls -ld /data` to verify the config



