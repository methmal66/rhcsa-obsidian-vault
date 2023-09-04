#linux #flashcards #rhcsa #rhcsa/rh124/Ch7_Permissions 

Which special file permission is used to run a file(mostly script) as the owner of it(mostly root), no matter who is logged in currently?::suid
<!--SR:!2023-09-22,49,311-->

Which special file permission is used to run a file as the group of it, no matter who is logged in currently?::guid
<!--SR:!2023-09-25,52,311-->

Which special file permission is set to directories to inherit group ownership to their files?::guid
<!--SR:!2023-09-23,50,291-->

Which special file permission is used to prevent who have write access to a directory from removing files they don't own?::sticky
<!--SR:!2023-09-27,54,311-->

How to set suid to a script?::`chmod u+s script`
<!--SR:!2023-10-16,58,291-->

How to set sgid to a script or a directory?::`chmod g+s file`
<!--SR:!2023-10-17,59,291-->

How to set sticky to a directory?::`chmod o+t dir`
<!--SR:!2023-09-29,56,311-->

What is the numerical value of suid?::4
<!--SR:!2023-08-29,25,291-->

What is the numerical value of guid?::2
<!--SR:!2023-09-30,57,311-->

What is the numerical value of sticky?::1
<!--SR:!2023-09-23,50,311-->

References:
- [Chapter7 ,Section3 ,Managing default permissions and file access ](rh124-rhel8-official-student-workbook.pdf#pageno=244)
Related:
- [[Permissions]]
- [[Default permissions]]
