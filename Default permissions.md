 #linux #flashcards #rhcsa #rhcsa/rh124/Ch7_Permissions 

How to find the umask of the current session?::`umask`
<!--SR:!2023-07-26,4,291-->

What is the default umask of root?::022
<!--SR:!2023-07-26,4,291-->

What is the default file permission of root?::rw-r--r-- (644)
<!--SR:!2023-07-26,4,291-->

What is the default directory permission of root?::777 - 022 = 755(rwx-r-xr-x)
<!--SR:!2023-07-26,4,291-->

What is the default umask of a regular user?::002
<!--SR:!2023-07-26,4,291-->

What is the default file permission of a regular user?::666 - 002 = 664(rw-rw-r--)
<!--SR:!2023-07-26,4,291-->

What is the default directory permission of a regular user?::777 - 002 = 775(rwxrwxr-x )
<!--SR:!2023-07-26,4,291-->

What is the universal default permissions of a directory before the umask is applied?::777(rwxrwxrwx)
<!--SR:!2023-07-26,4,291-->

What is the universal default permissions of a file before the umask is applied?::666(rw-rw-rw-)
<!--SR:!2023-07-26,4,291-->

What are the default permissions which are impossible to have?::Execute permissions on files for both root and regular users
<!--SR:!2023-07-26,4,291-->

How to set permanent umask for each session?::`echo "umask 007" > ~/.bashrc`
<!--SR:!2023-07-26,4,291-->

What is the purpose of umask?::Limit certain permissions for newly created files by default
<!--SR:!2023-07-26,4,291-->

How to calculate the umask?:: 3digit default permissions - 3digit desired permissions
<!--SR:!2023-07-26,4,291-->

Some home directories are changed when switching users?::Root handles that as a middle man
<!--SR:!2023-07-26,4,291-->

References
 - [Chapter7, Section3, Managing default permissions and file access](rh124-8.0-student-guide.pdf#pageno=244)
Related:
- [[Permissions]]
- [[Special permissions]]