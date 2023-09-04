---
tags:
  - flashcards
  - rh124/Ch12_Archives
  - rh124
---

What is the most critical advantages of archiving?::It reduce the inode usage

<!--SR:!2023-08-08,4,270-->

What happens when archiving?::Sources files are copied to an archive file

<!--SR:!2023-08-08,4,270-->

What is the standard extension for an archive file?::.tar

<!--SR:!2023-08-08,4,270-->

How to archive multiple files?::`tar -cf output-file.tar file1 file2 file3`

<!--SR:!2023-08-05,1,230-->

How to archive the entire /etc directory?::`tar -cf etc.tar /etc`

<!--SR:!2023-08-07,3,250-->

How to list the files inside an archive, without extracting it?::`tar -tf archive.tar`

<!--SR:!2023-08-08,4,270-->

How to extract an archive file?::`tar -xf archive.tar`

<!--SR:!2023-08-05,1,230-->

What happens when extracting an archive file?::Files inside the archive are copied into the location as the output of `tar -tf archive.tar` command

What happens to file attributes when extracting?::They are preserved

<!--SR:!2023-08-08,4,270-->
