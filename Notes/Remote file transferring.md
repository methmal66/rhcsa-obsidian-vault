#rhcsa #linux #rhcsa/rh124/Ch12_Archives  #flashcards 

How to securely copy a file to a remote server
?
`scp file user@server:/dir/path` or 
`rsync file user@server:/dir/path`
<!--SR:!2023-08-08,4,270-->

How to securely copy a directory to a remote server
?
`scp -r dir user@server:/dir/path` or 
`rsync -av user@server:/dir/path`
<!--SR:!2023-08-07,3,250-->

What is the advantage of using rsync over scp?::`It copy only the updated files when tranfering them`
<!--SR:!2023-08-08,4,270-->

What technology does both scp and rsync is based on?::ssh
<!--SR:!2023-08-08,4,270-->

References:
- [Chapter13, Section2, Transferring files between systems securely](rh124-rhel8-official-student-workbook.pdf#pageno=486)
- [Chapter13, Section3, Synchronizing files between systems securely](rh124-rhel8-official-student-workbook.pdf#pageno=486)
Related:
- [[Implement key authentication]]
- [[Archiving]]