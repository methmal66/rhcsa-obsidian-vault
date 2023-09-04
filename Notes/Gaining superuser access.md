---
tags:
  - flashcards
  - rh124/Ch6_Users
  - rh124
---

What is the uid of the root?::0

<!--SR:!2023-10-21,76,310-->

Which users has all the privilege?::Superusers

<!--SR:!2023-10-26,81,310-->

How a regular user can execute a command as root without login?
?
`sudo ls` or
`sudo -u root ls`

<!--SR:!2023-08-09,18,270-->

How to execute a command as another user without login?::`sudo -u username ls`

<!--SR:!2023-08-13,22,308-->

# Method1: Grant direct access

How to grant superuser privilege to a regular user?::`echo "methmal  ALL  ALL=(ALL)" > /etc/sudoers.d/methmal` or add the user to a group which is already sudo

<!--SR:!2023-08-12,21,311-->

# Method2: Add to sudo group

Which config file is used to set superuser privilege?::`/etc/sudoers`

<!--SR:!2023-10-21,76,310-->

# Method3: Create a sudoer file

Which config directory is used to set each user's special privileges?::`/etc/sudoers.d`

<!--SR:!2023-08-10,4,289-->
