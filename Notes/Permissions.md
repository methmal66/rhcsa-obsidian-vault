---
tags:
  - flashcards
  - rh124/Ch7_Permissions
  - rh124
---

How to find the permissions of a file?::`ls -l /path/to/file` or `ll /path/to/file`

<!--SR:!2023-09-30,57,311-->

How to find the permissions of all the files inside a directory?::`ls -la /path/to/dir`

<!--SR:!2023-09-24,51,311-->

How to find the permissions of a directory, without its content?::`ls -ld /path/to/dir`

<!--SR:!2023-09-26,53,311-->

How to change the both user and group of ownership of a file?::`chown user:group file`

<!--SR:!2023-12-16,119,325-->

How to change only the user ownership of a file?::`chown user file`

<!--SR:!2023-12-20,123,325-->

How to change only the group ownership of a file?::`chown :group file`

<!--SR:!2023-12-09,112,310-->

How to change the ownership of a directory, recessively to it's content?::`chown -R user:group dir`

<!--SR:!2023-12-17,120,321-->

What is the special permission of a file/directory only the owner and root have?::Ability to change the permissions of the file/directory

<!--SR:!2023-12-14,117,321-->

What is the impact of granting read(r) permission of a directory?::Ability to list the files inside of it

<!--SR:!2023-12-15,118,325-->

What is the impact of granting write(w) permission of a directory?::Ability to create and delete files inside it

<!--SR:!2023-12-10,113,310-->

What is the impact of granting execute(x) permission of a directory?::Ability to change the directory to it

<!--SR:!2023-12-08,111,310-->

How to add write access to a file, for the user only?::`chmod u+w file`

<!--SR:!2023-12-18,121,321-->

How to remove read access from a file, for the group only::`chmod g-r file`

<!--SR:!2023-12-06,109,310-->

How to remove all access to a file, for the others only?::`chmod o= file` or `chmod o-a file` or `chmod o-rwx file`

<!--SR:!2023-11-06,79,310-->

How to add executable access to all?::`chmod +x script`

<!--SR:!2023-12-10,113,310-->

Which type of files except directories need the executable access?::Scripts and binary files

<!--SR:!2023-12-07,110,301-->

How to configure permissions as rw-rw-r-- acess to a file?
?
`chmod 664 file` or
`chmod ug=rw,o=r file`

<!--SR:!2023-12-04,107,305-->

How to add all access to a file for all owner, group and others?::`chmod 777 file` or `chmod a=rwx file`

<!--SR:!2023-12-05,108,301-->

How to add executable access to a directory?::`chmod o+x file`

<!--SR:!2023-12-19,122,325-->

How to add read access to a directory?::`chmod +rx dir`

<!--SR:!2023-12-08,111,310-->

How to remove read access to a directory?::`chmod -r dir`

<!--SR:!2023-12-13,116,310-->

How to add write access to a directory?::`chmod +wx dir`

<!--SR:!2023-10-06,48,265-->

How to remove write access to a directory::`chmod -w dir`

<!--SR:!2023-11-04,77,290-->

Which permission is pointless when it is set to a directory alone?::Execute

<!--SR:!2023-12-03,106,290-->
