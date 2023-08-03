#linux #flashcards #rhcsa #rhcsa/rh124/Ch3_File-basics 

Which type of links increase the number displayed form the `ls -l link` command?::hard link
<!--SR:!2023-07-20,4,270-->

How to create a hard link?::`ln /existing/file /output/file`
<!--SR:!2023-08-16,25,290-->

Which type of links preserve the inode, file permissions, ownership and other attributes of the source file?::`hard links`
<!--SR:!2023-08-18,27,306-->

What type of links sync the update done to their source file?::Both soft links and hard links
<!--SR:!2023-07-20,4,289-->

Why are they called "hard links"?::Because they don't break tough the original file is moved

Why hard links do not break though their origin is moved?::Because hard links are pointed to the file content, not to the file name.
<!--SR:!2023-08-18,27,306-->

Which type of files can have a hard link?::Only a normal files, directories or special files cannot
<!--SR:!2023-07-19,1,210-->

What is the requirement to create a hard link to a normal file?::Both files should be in the same file system, not necessarily the partitions
<!--SR:!2023-08-11,20,290-->

Which type of links are used to create links for directories?::soft links
<!--SR:!2023-07-20,4,270-->

How to create a soft link?::`ln -s /existing/file /output/file`
<!--SR:!2023-07-20,4,270-->

Which type of links create additional inodes?::`soft links`
<!--SR:!2023-07-20,4,270-->

Which type of links display their source path when the link is listed?::Soft links

Why softlinks break when the original file is moved?::That soft link breaks, as soft links are pointed to the file name, not to the file content
<!--SR:!2023-08-16,25,290-->

References:
- [Chapter3, Section3, Making links between files](rh124-8.0-student-guide.pdf#pageno=95)
Related:
- [[Copying files]]
- [[Moving files]]
- [[Deleting files]]
- [[Creating links]]
- [[File hierarchy]]
