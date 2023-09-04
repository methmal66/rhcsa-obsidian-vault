---
tags:
  - flashcards
  - rh124/Ch6_Users
  - rh124
---

What is the default uid range of regular users?::`[1000,60000]`

<!--SR:!2023-10-24,79,310-->

What is the uid range of system users?::`[0,1000)`

<!--SR:!2023-10-24,79,310-->

How to create a user?::`useradd username`

<!--SR:!2023-08-21,30,290-->

Which config file maintains the user info like username, uid, gid, comment, home, shell?::/etc/passwd

<!--SR:!2023-10-19,74,310-->

Which config file keeps user passwords in encrypted format?::/etc/shadow

<!--SR:!2023-10-23,78,310-->

Why newly created users are assigned with a primary group which has a similar name and id of the user?::To make the file ownership and permissions easy.

<!--SR:!2023-10-22,77,310-->

How to manually configure the password after adding a user?::`passwd username`

<!--SR:!2023-10-20,75,310-->

How to configure user password without the interactive prompt?::`echo "password" | passwd --stdin methmal`

How to make a user cannot login to the shell?::`usrmod username -s /usr/sbin/nologin`

<!--SR:!2023-10-18,73,290-->

How to display info about an user?::`id username`

<!--SR:!2023-09-21,46,290-->

How to delete a user?::`userdel username`

<!--SR:!2023-10-23,78,310-->

How to find if a user exist?::`cat /etc/passwd | grep username`

<!--SR:!2023-10-20,75,310-->

How to list files owned by a user inside a particular directory?::`find / -user methmal`

How to config the full name of a user?::`usermod -c "Full Name"`

<!--SR:!2023-08-07,20,290-->

How to create a new group?::`groupadd groupname`

<!--SR:!2023-10-27,82,322-->

How to delete a group?::`groupdel groupname`

<!--SR:!2023-10-25,80,322-->

How to avoid having users with mismatched uid and gid?::Create the first regular group with a higher gid

<!--SR:!2023-10-22,77,310-->

How to append a user to a group?::`usermod -aG groupname username`

<!--SR:!2023-08-08,21,290-->
