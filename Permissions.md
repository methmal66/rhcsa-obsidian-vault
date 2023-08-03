 #linux #flashcards #rhcsa #rhcsa/rh124/Ch7_Permissions

How to find the permissions of a file?::`ls -l /path/to/file` or `ll /path/to/file`
<!--SR:!2023-07-26,4,291-->

How to find the permissions of all the files inside a directory?::`ls -la /path/to/dir`
<!--SR:!2023-07-26,4,291-->

How to find the permissions of a directory, without its content?::`ls -ld /path/to/dir`
<!--SR:!2023-07-26,4,291-->

How to change the both user and group of ownership of a file?::`chown user:group file`
<!--SR:!2023-08-15,24,305-->

How to change only the user ownership of a file?::`chown user file`
<!--SR:!2023-08-18,27,305-->

How to change only the group ownership of a file?::`chown :group file`
<!--SR:!2023-08-13,22,290-->

How to change the ownership of a directory, recessively to it's content?::`chown -R user:group dir`
<!--SR:!2023-08-11,20,301-->

What is the special permission of a file/directory only the owner and root have?::Ability to change the permissions of the file/directory 
<!--SR:!2023-08-12,21,301-->

What is the impact of granting read(r) permission of a directory?::Ability to list the files inside of it
<!--SR:!2023-08-17,26,305-->

What is the impact of granting write(w) permission of a directory?::Ability to create and delete files inside it
<!--SR:!2023-08-16,25,290-->

What is the impact of granting execute(x) permission of a directory?::Ability to change the directory to it
<!--SR:!2023-08-14,23,290-->

How to add write access to a file, for the user only?::`chmod u+w file`
<!--SR:!2023-08-11,20,301-->

How to remove read access from a file, for the group only::`chmod g-r file`
<!--SR:!2023-08-13,22,290-->

How to remove all access to a file, for the others only?::`chmod o= file` or `chmod o-a file` or `chmod o-rwx file`
<!--SR:!2023-08-14,23,310-->

How to add executable access to all?::`chmod +x script`
<!--SR:!2023-08-11,20,290-->

Which type of files except directories need the executable access?::Scripts and binary files
<!--SR:!2023-08-07,16,281-->

How to configure permissions as rw-rw-r-- acess to a file?
?
`chmod 664 file` or
`chmod ug=rw,o=r file`
<!--SR:!2023-08-06,15,285-->

How to add all access to a file for all owner, group and others?::`chmod 777 file` or `chmod a=rwx file` 
<!--SR:!2023-08-05,14,281-->

How to add executable access to a directory?::`chmod o+x file`
<!--SR:!2023-08-15,24,305-->

How to add read access to a directory?::`chmod +rx dir` 
<!--SR:!2023-08-12,21,290-->

How to remove read access to a directory?::`chmod -r dir`
<!--SR:!2023-08-14,23,290-->

How to add write access to a directory?::`chmod +wx dir`
<!--SR:!2023-07-24,2,265-->

How to remove write access to a directory::`chmod -w dir`
<!--SR:!2023-08-16,25,290-->

Which permission is pointless when it is set to a directory alone?::Execute
<!--SR:!2023-08-06,15,270-->

References:
- [Chapter7, Section2, Managing file system permissions from the command line](rh124-8.0-student-guide.pdf#pageno=236)
- [Chapter7, Section1, Interpreting linux file system permisssions](rh124-8.0-student-guide.pdf#pageno=236)
Also read:
- [[Default permissions]]
- [[Special permissions]]
