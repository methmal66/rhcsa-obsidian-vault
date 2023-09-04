---
tags:
  - flashcards
  - rh124/Ch3_File-basics
  - rh124
---

Which type of links increase the number displayed in the output of `ls -l` command?::hard link

<!--SR:!2023-08-10,4,250-->

How to create a hard link?::`ln /existing/file /output/file`

<!--SR:!2023-08-16,25,290-->

Which type of links preserve the inode, file permissions, ownership and other attributes of the source file?::`hard links`

<!--SR:!2023-08-18,27,306-->

What type of links sync the update done to their source file?::Both soft links and hard links

<!--SR:!2023-10-19,76,309-->

Why are they called "hard links"?::Because they don't break tough the original file is moved

<!--SR:!2023-08-08,4,287-->

Why hard links do not break though their origin is moved?::Because hard links are pointed to the file content, not to the file name.

<!--SR:!2023-08-18,27,306-->

Which type of files can have a hard link?::Only a normal files, directories or special files cannot

<!--SR:!2023-08-07,3,190-->

What is the requirement to create a hard link to a normal file?::Both files should be in the same file system, not necessarily the partitions

<!--SR:!2023-08-11,20,290-->

Which type of links are used to create links for directories?::soft links

<!--SR:!2023-10-14,71,290-->

How to create a soft link?::`ln -s /existing/file /output/file`

<!--SR:!2023-10-28,83,290-->

Which type of links create additional inodes?::`soft links`

<!--SR:!2023-10-17,74,290-->

Which type of links display their source path when the link is listed?::Soft links

<!--SR:!2023-08-08,4,287-->

Why softlinks break when the original file is moved?::That soft link breaks, as soft links are pointed to the file name, not to the file content

<!--SR:!2023-08-16,25,290-->
