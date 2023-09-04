---
tags:
  - flashcards
  - rh124/Ch5_File-editing
  - rh124
related:
  - "[[Copying files]]"
---

What is the purpose of redirecting output?::Store or display the output and error messages generate in a command in separate locations

<!--SR:!2023-10-12,69,310-->

What are the I/O channels?::stdin(0), stdout(1/default) and stderror(2)

<!--SR:!2023-10-16,73,310-->

How to specify the both output and error when redirecting I/O channels?::&

<!--SR:!2023-10-12,69,310-->

What are the two writing methods of a file?::Overwrite(>) and Append(>>)

<!--SR:!2023-10-12,69,310-->

How to copy last 100 lines of a file?::`tail -n 100 /var/log/dmesg > /tmp/last-100-boot-messages`

<!--SR:!2023-09-22,49,290-->

How to create a file by concating multiple files?::`cat file1 file2 file3 file4 > /tmp/all-four-in-one`

<!--SR:!2023-09-21,48,290-->

How to append a line to a file?::`echo "This is a new file" >> ~/Documents/text.txt`

<!--SR:!2023-10-11,68,310-->

How to save both output and errors of a command in the same file?::`find /etc -name passwd &> output-and-errors`

<!--SR:!2023-10-10,67,310-->

How to discard the error messages from a command?::`find /etc -name passwd 2> /dev/null`

<!--SR:!2023-10-11,68,310-->

What does a pipeline do to a command?::`Redirect the output of a command as an input to another command`

<!--SR:!2023-10-13,70,310-->

How to show a long output line by line, without make the terminal ugly?::`ls -l /usr/bin | less`

<!--SR:!2023-10-14,71,310-->

How to search for patterns in a file?::`cat /var/log/messages | grep system`

<!--SR:!2023-10-15,72,310-->

How to find the number of error messages a command display?::`find / -name paswd > /dev/null | wc -l`

<!--SR:!2023-10-07,64,290-->

Why command `tee` is used with piplines?::To redirect the content flowing through a pipeline into a separate file or display

<!--SR:!2023-09-19,46,290-->

How to store and display the output of a command at the same time?::`ls -l /usr/bin | tee output`

<!--SR:!2023-09-17,44,290-->

How to store the intermittent output of two commands?::`ls -l | tee /tmp/saved-output | wc -l`

<!--SR:!2023-10-10,67,310-->

How to display the intermittent output of two commands in the terminal?::`ls -l | tee /dev/tty | wc -l`

<!--SR:!2023-09-20,47,290-->
