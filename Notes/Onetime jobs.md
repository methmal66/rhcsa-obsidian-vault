#linux #rhcsa #flashcards #rhcsa/rh134/Ch2_Scheduling

Which service is used to handle future jobs?::atd

How many queues are provided by atd?::26 (from a to z)

What is the unique identifier used with jobs?::Job number

How to save a job after entering the command?:: Ctrl + D

How to list the schedule jobs?::`atq` or `at -l`
![300](https://i.imgur.com/cMGKGST.png)

Which jobs can be inspected by an unprivileged user?::Only jobs scheduled by that user

Which user can inspect the jobs of all the users?::Root user

How to display the environment of a job using the job number?::`at -c 4`
![500](https://i.imgur.com/UCfQRhk.png)


How to schedule 'myscript' to run at today 9pm?::`at 21:00 < myscript`

How to schedule a job at today 2pm in the queue b?::`at -q b 2pm`

How to schedule a job at 5 minutes from now?::`at now +5mins`

How to schedule a job at the tomorrow's teatime(4pm)?::`at teatiime tomorrow`

How to schedule a job at 2023-08-05 5pm?::`at 5pm august 5 2023` or `at 5pm 2023-08-05`

How to remove a job with job number 30?::`atrm 30`

