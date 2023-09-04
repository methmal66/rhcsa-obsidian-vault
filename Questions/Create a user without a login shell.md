---
tags:
  - rhcsa
  - linux
  - question
  - rhcsa/rh124/Ch6_Users
reference:
  - "[[Accounts]]"
related:
  - "[[Create a user with uid and password]]"
  - "[[Create the users and groups as the requirement]]"
---
Create the user named **eric** and deny to interactive login

>[!info]- Answer
>1. `useradd eric`
>2. `usermod eric -s /sbin/nologin`. Path to `nologin` can be found from `cat /etc/shadow | grep nologin` or `find / -name nologin`
>3. `cat /etc/shadow | grep eric` to verify the configs
