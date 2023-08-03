#linux #flashcards #rhcsa #rhcsa/rh124/Ch12_Archives 

What is the most critical advantages of archiving?::It reduce the inode usage

What happens when archiving?::Sources files are copied to an archive file

What is the standard extension for an archive file?::.tar

How to archive multiple files?::`tar -cf output-file.tar file1 file2 file3`

How to archive the entire /etc directory?::`tar -cf etc.tar /etc`

How to list the files inside an archive, without extracting it?::`tar -tf archive.tar`

How to extract an archive file?::`tar -xf archive.tar`

What happens when extracting an file?::Files inside the archive are copied into the location as the output of `tar -tf archive.tar` command

What happens to file attributes when extracting?::They are preserved

What is the standard file extension for file compressed using gzip algorithm?::gz

How to compress a file using xz without losing the original content?::``

How to decompress a file using xz without losing the original compressed file?::

What is the standard file extension for a file compressed using bzip2 algorithm?::.bz2

What is the standard file extension for a file compressed using xz algorithm?::.xz

Which algorithm has the highest compression rate?::xz