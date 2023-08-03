#linux  #flashcards #rhcsa #rhcsa/rh124/Ch5_File-editing
 
How to set a local variable?::`VARIABLE=value`
<!--SR:!2023-08-04,17,290-->

How to unset a variable?::`unset VARIABLE`
<!--SR:!2023-08-03,16,290-->

How to export a global variable?::`export APP_PASSWORD="my str0ng p@s$word"`
<!--SR:!2023-08-04,17,290-->

How to display a single variable?::`echo $VARIABLE`
<!--SR:!2023-08-16,25,306-->

How to display all the environmental variables?::`printenv`
<!--SR:!2023-08-01,14,290-->

Which config file is used to set user specific variables?::~/.bashrc
<!--SR:!2023-07-31,13,290-->

How to update PATH?::`echo "PATH="$HOME/bin:$PATH"" >> ~/.bashrc` and then `source ~/.bashrc`
Which config file is used to set global persist variables?::/etc/environment 
<!--SR:!2023-07-31,13,290-->

What is a local variable?::Variables which can only be accessed inside the session(or script) where they were defined
<!--SR:!2023-08-01,14,290-->

What is a global variables?::Ones across sessions( or users)
<!--SR:!2023-08-02,15,290-->

What is a user specific variable?::Variables which can be accessed by a the user who defined it anytime
<!--SR:!2023-08-01,14,290-->

Which type of variables are persist across reboots?::Variables configured in a file
<!--SR:!2023-07-31,13,290-->

Which type of variables are not persist across reboots?::Variables set using a command
<!--SR:!2023-08-03,16,290-->

References:
- [Chapter5, Section3, Changing the shell environment](rh124-8.0-student-guide.pdf#pageno=142)
Related:
- [[Bash features]]
- [[Accounts]]