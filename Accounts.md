#rhcsa #flashcards #linux #rhcsa/rh124/Ch6_Users 
What is the default uid range of regular users?::`[1000,60000]`
<!--SR:!2023-08-01,14,290-->

What is the uid range of system users?::`[0,1000)`
<!--SR:!2023-08-03,16,290-->

How to create a user?::`useradd username`
<!--SR:!2023-08-21,30,290-->

Which config file maintains the user info like username, uid, gid, comment, home, shell?::/etc/passwd
<!--SR:!2023-07-31,13,290-->

Which config file keeps user passwords in encrypted format?::/etc/shadow
<!--SR:!2023-08-03,16,290-->

Why newly created users are assigned with a primary group which has a similar name and id of the user?::To make the file ownership and permissions easy.
<!--SR:!2023-08-04,17,290-->

How to manually configure the password after adding a user?::`passwd username`
<!--SR:!2023-08-01,14,290-->

How to make a user cannot login to the shell?::`usrmod username -s /usr/sbin/nologin`
<!--SR:!2023-07-30,12,270-->

How to display info about an user?::`id username`
<!--SR:!2023-07-31,13,290-->

How to delete a user?::`userdel username`
<!--SR:!2023-08-03,16,290-->

How to find if a user exist?::`cat /etc/passwd | grep username`
<!--SR:!2023-08-06,19,290-->

How to config the full name of a user?::`usermod -c "Full Name"`
<!--SR:!2023-08-07,20,290-->

How to create a new group?::`groupadd groupname`
<!--SR:!2023-08-05,18,302-->

How to delete a group?::`groupdel groupname`
<!--SR:!2023-08-05,18,302-->

How to avoid having users with mismatched uid and gid?::Create the first regular group with a higher gid
<!--SR:!2023-08-02,15,290-->

How to append a user to a group?::`usermod -aG groupname username`
<!--SR:!2023-08-08,21,290-->

References:
- [Chapter6, Section1, Describing user and group concepts](rh124-8.0-student-guide.pdf#pageno162)
- [Chapter6, Section3, Managing local user accounts](rh124-8.0-student-guide.pdf#pageno180)
- [Chapter6, Section4, Managing local group accounts](rh124-8.0-student-guide.pdf#pageno189)
Related:
- [[Gaining superuser access]]
- [[uid and gid mismatch]]
- [[Password policies]]