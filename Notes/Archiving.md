---
tags:
  - flashcards
  - rh124/Ch12_Archives
  - rh124
---
>[!faq] How to archive multiple files?::`tar -cf output-file.tar file1 file2 file3`

>[!faq] How to archive the entire /etc directory?::`tar -cf etc.tar /etc`

>[!faq] How to list the files inside an archive, without extracting it?::`tar -tf archive.tar`

>[!faq] How to extract an archive file?::`tar -xf archive.tar`

What is the most critical advantages of archiving?
	It reduce the inode usage

What happens when archiving?
	Sources files are copied to an archive file

What is the standard extension for an archive file?
	.tar
	
What happens when extracting an archive file?
	Files inside the archive are copied into the location as the output of `tar -tf archive.tar` command

What happens to file attributes when extracting?
	They are preserved
