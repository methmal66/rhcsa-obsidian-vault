---
tags:
  - flashcards
  - rh124/Ch3_File-basics
  - rh124
related:
  - "[[inode depletion]]"
---

What are the files in /usr directory?::Installed software(software), shared libraries, include files and read-only program data

<!--SR:!2023-08-12,6,246-->

What are the files inside /usr/bin directory?::Binary files of user commands

<!--SR:!2023-10-03,60,270-->

What are the files inside /usr/sbin directory?::Binary files of system administration commands

<!--SR:!2023-08-06,2,230-->

What are the files inside /usr/local directory?::Locally customised software

<!--SR:!2023-08-06,15,270-->

Where the system wide configuration files are located?::In the /etc directory

<!--SR:!2023-08-15,24,290-->

Where are the variable data of the system which should be persist between reboots is located?::In the /var directory

<!--SR:!2023-08-17,26,306-->

Where are the runtime data of processes start from last boot are stored?::In the /run directory

<!--SR:!2023-08-18,27,306-->

Where are the regular user's personal files are stored?::In the /home/username directory of each user

<!--SR:!2023-08-12,21,290-->

What is the home directory of the root?::root

What is the directory made for storing temporary files which get deleted after 10 days if they haven't been used?::/tmp

<!--SR:!2023-08-11,20,290-->

Where are the files needed for the booting process is located?::In the /boot directory

<!--SR:!2023-08-17,26,306-->

Where are the special devices files and character files are located?::In the /dev directory

<!--SR:!2023-10-04,59,305-->

What is an absolute path?::A fully qualified name of a file which specifies the exact location of it, no matter where you are.

<!--SR:!2023-08-12,21,309-->

How to identify an absolute path?::They all begin from the `/` (root directory)

<!--SR:!2023-08-15,24,290-->

What is the initial working directory when logged as an user?::Logged in user's home directory

<!--SR:!2023-08-13,22,290-->

How to print the working directory where the user is currently in?::`pwd`

<!--SR:!2023-08-14,23,290-->

Why creating `FileCase.txt` and `filecase.txt` in the same directory results in two unique files?::Because most of linux file systems are case sensitive

<!--SR:!2023-08-13,22,290-->

Which command is used to list the content of a directory?::`ls`

<!--SR:!2023-08-15,24,290-->

How to list content of a directory and all of it's sub directories?::`ls -R dir`

<!--SR:!2023-08-15,24,290-->

Which command is used to change the working directory?::`cd`

<!--SR:!2023-08-11,20,290-->
