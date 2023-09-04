---
tags:
  - flashcards
  - rh124/Ch7_Permissions
  - rh124
---

How to find the umask of the current session?::`umask`

<!--SR:!2023-09-29,56,311-->

What is the default umask of root?::022

<!--SR:!2023-09-28,55,311-->

What is the default file permission of root?::666 - 022 = 644 (rw-r--r--)

<!--SR:!2023-10-05,47,291-->

What is the default directory permission of root?::777 - 022 = 755(rwx-r-xr-x)

<!--SR:!2023-10-18,60,291-->

What is the default umask of a regular user?::002

<!--SR:!2023-12-12,115,311-->

What is the default file permission of a regular user?::666 - 002 = 664(rw-rw-r--)

<!--SR:!2023-10-18,60,291-->

What is the default directory permission of a regular user?::777 - 002 = 775(rwxrwxr-x )

<!--SR:!2023-09-27,54,311-->

What is the universal default permissions of a directory before the umask is applied?::777(rwxrwxrwx)

<!--SR:!2023-09-26,53,311-->

What is the universal default permissions of a file before the umask is applied?::666(rw-rw-rw-), Execute permission is not granted to files by default

<!--SR:!2023-07-26,4,291-->

What are the default permissions which are impossible to have?::Execute permissions on files for both root and regular users

<!--SR:!2023-09-26,53,311-->

How to set permanent umask for each session?::`echo "umask 007" > ~/.bashrc`

<!--SR:!2023-08-28,24,291-->

What is the purpose of umask?::Limit certain permissions for newly created files by default

<!--SR:!2023-09-25,52,311-->

How to calculate the umask?::By considering which permissions to avoid

<!--SR:!2023-12-11,114,311-->

How home directories are changed when switching users?::Root handles that as a middle man

<!--SR:!2023-07-26,4,291-->
