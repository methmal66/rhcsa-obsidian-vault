---
tags:
  - flashcards
  - rh124/Ch5_File-editing
  - rh124
related:
  - "[[Bash features]]"
  - "[[Accounts]]"
---

How to set a local variable?::`VARIABLE=value`

<!--SR:!2023-08-12,8,270-->

How to unset a variable?::`unset VARIABLE`

<!--SR:!2023-10-08,65,310-->

How to set a global variable?::`export APP_PASSWORD="my str0ng p@s$word"`

<!--SR:!2023-08-04,17,290-->

How to display a single variable?::`echo $VARIABLE`

<!--SR:!2023-08-16,25,306-->

How to display all the environmental variables?::`printenv`

<!--SR:!2023-10-09,66,310-->

Which config file is used to set user specific variables?::~/.bashrc

<!--SR:!2023-10-09,66,310-->

How to update PATH?::`echo "PATH="$HOME/bin:$PATH"" >> ~/.bashrc` and then `source ~/.bashrc`

<!--SR:!2023-08-08,4,295-->

Which config file is used to set global persist variables?::/etc/environment

<!--SR:!2023-08-10,6,270-->

What is a local variable?::Variables which can only be accessed inside the session(or script) where they were defined

<!--SR:!2023-08-09,5,270-->

What is a global variables?::Ones can be accessed across sessions( or users)

<!--SR:!2023-08-02,15,290-->

What is a user specific variable?::Variables which can be accessed by a the user who defined it anytime

<!--SR:!2023-09-18,45,290-->

Which type of variables are persist across reboots?::Variables configured in a file

<!--SR:!2023-10-15,72,310-->

Which type of variables are not persist across reboots?::Variables set using a command

<!--SR:!2023-10-09,66,310-->
