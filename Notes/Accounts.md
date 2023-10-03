---
tags:
  - flashcards
  - rh124/Ch6_Users
  - rh124
  - important
---

> [!faq] How to create a user?
> ?
> `useradd username`
> Delete that user by `userdel username`

>[!faq] Which config file maintains the user info like username, uid, gid, comment, home, shell?::`/etc/passwd`

>[!faq] Which config file keeps user passwords in encrypted format?::`/etc/shadow`

>[!faq] How to manually configure the password after adding a user?::`passwd username`

>[!faq] How to make a user cannot login to the shell?::`usrmod username -s /usr/sbin/nologin`

>[!faq] How to list files owned by a user inside a particular directory?::`find / -user methmal`

>[!faq] How to create a new group?
>?
>`groupadd groupname`
>Delete a group by `groupdel groupname`

>[!faq]  How to append a user to a group?
>?
>`usermod -aG groupname username`
>Remove a user from the group by `gpasswd -d username groupname`

What is the default uid range of regular users?
	`[1000,60000]`

What is the uid range of system users?
	`[0,1000)`

Why newly created users are assigned with a primary group which has a similar name and id of the user?
	To make the file ownership and permissions easy.
How to configure user password without the interactive prompt?
	`echo "password" | passwd --stdin methmal`

How to display info about an user?
	`id username`

How to find if a user exist?
	`cat /etc/passwd | grep username`

How to config the full name of a user?
	`usermod -c "Full Name"`

How to avoid having users with mismatched uid and gid?
	Create the first regular group with a higher gid
