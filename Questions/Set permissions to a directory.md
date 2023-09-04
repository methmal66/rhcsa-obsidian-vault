---
tags:
  - question
  - rh124/Ch7_Permissions
reference:
  - "[[Copying files]]"
  - "[[Permissions]]"
related:
  - "[[Allow access to others home directory]]"
  - "[[Grant full access to user and group only]]"
---

According the following requirements to create a local directory **/common/admin**.

- This directory has **admin** group.
- This directory has read, write and execute permissions for all admin group members.
- Other groups and users don’t have any permissions.
- All the documents or directories created in the/common/admin are automatically inherit the admin group.

> [!info]- Answers
>
> 1.  `mkdir /common/admin`
> 2.  `chown :admin /common/admin`
> 3.  `chmod 2070 /common/admin `
> 4.  `ls -l /common/admin` to verify the configs
