#linux #flashcards #rhcsa #rhcsa/rh124/Ch5_File-editing 

#todo i/o channels and pipeline drawings

What is the purpose of redirecting output?::Store or display the output and error messages generate in a command in separate locations
<!--SR:!2023-08-02,15,290-->

What are the I/O channels?::stdin(0), stdout(1/default) and stderror(2)
<!--SR:!2023-08-04,17,290-->

How to specify the both output and error when redirecting I/O channels?::&
<!--SR:!2023-08-03,16,290-->

What are the two writing methods of a file?::Overwrite(>) and Append(>>)
<!--SR:!2023-08-02,15,290-->

How to copy last 100 lines of a file?::`tail -n 100 /var/log/dmesg > /tmp/last-100-boot-messages`
<!--SR:!2023-08-04,17,290-->

How to create a file by concating multiple files?::`cat file1 file2 file3 file4 > /tmp/all-four-in-one`
<!--SR:!2023-08-04,17,290-->

How to append a line to a file?::`echo "This is a new file" >> ~/Documents/text.txt`
<!--SR:!2023-08-03,16,290-->

How to save both output and errors of a command in the same file?::`find /etc -name passwd &> output-and-errors`
<!--SR:!2023-08-03,16,290-->

How to discard the error messages from a command?::`find /etc -name passwd 2> /dev/null`
<!--SR:!2023-07-31,13,290-->

What does a pipeline do to a command?::`Redirect the output of a command as an input to another command`
<!--SR:!2023-08-02,15,290-->

How to show a long output line by line, without make the terminal ugly?::`ls -l /usr/bin | less`
<!--SR:!2023-08-02,15,290-->

How to search for patterns in a file?::`cat /var/log/messages | grep system`
<!--SR:!2023-08-04,17,290-->

How to find the number of error messages a command display?::`find / -name paswd > /dev/null | wc -l`
<!--SR:!2023-07-30,12,270-->

Why command `tee` is used with piplines?::To redirect the content flowing through a pipeline into a separate file or display
<!--SR:!2023-08-01,14,290-->

How to store and display the output of a command at the same time?::`ls -l /usr/bin | tee output`
<!--SR:!2023-07-31,13,290-->

How to store the intermittent output of two commands?::`ls -l | tee /tmp/saved-output | wc -l`
<!--SR:!2023-08-01,14,290-->

How to display the intermittent output of two commands in the terminal?::`ls -l | tee /dev/tty | wc -l`
<!--SR:!2023-08-02,15,290-->

References:
- [Chapter5, Section1, Redirecting output to a file or program](rh124-8.0-student-guide.pdf#pageno=126)