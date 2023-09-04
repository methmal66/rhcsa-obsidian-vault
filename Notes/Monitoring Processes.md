#linux #flashcards #rhcsa #rhcsa/rh124/Ch8_Processes 

What is a process?::A program in execution
<!--SR:!2023-10-25,64,292-->

What is a job?::A process interactively started by a user and doesn't detach
<!--SR:!2023-10-26,65,292-->

What is a task?::
<!--SR:!2023-10-24,63,292-->

What is a thread?::
<!--SR:!2023-08-26,4,291-->

What is a core?::
<!--SR:!2023-10-24,63,292-->

What does it mean that a process is running?::Its either executing in the CPU or waiting for that
<!--SR:!2023-10-26,65,292-->

What does it mean that a process is sleeping?::Its waiting without running, until some conditions to satisfy 
<!--SR:!2023-10-22,61,292-->

What does it mean that a process is stopped?::Its being stopped from executing by a user or kernel
<!--SR:!2023-08-26,4,291-->
. It will continue from where it was stoped, when starting on future<!--SR:!2023-10-25,64,292-->

What does it mean that a process is in the zombie state?::It has signalled its parent as it exits. All resources except for the process identity (PID) are released.
<!--SR:!2023-10-25,64,292-->

What are the only process states which are considered when calculating the load average?::Running and Sleeping states
<!--SR:!2023-10-22,61,292-->

What is the process state that will be never observed in process-listening utilities?::Zombie state
<!--SR:!2023-08-26,4,291-->

Which process state is represented by the flag 'R'?::Running state
<!--SR:!2023-10-22,61,292-->

Which process state is represented by the flags 'S, D, K, I'?::Sleeping state
<!--SR:!2023-10-23,62,292-->

Which process state is represented by the flag 'T'?::Stop state
<!--SR:!2023-10-29,68,290-->

Which process state is represented by the flag 'Z, X'?::Zombie state
<!--SR:!2023-10-21,60,292-->

How to display the current process details one time?::`ps -aux`
<!--SR:!2023-10-23,62,292-->

How to display the current details of processes with the given command?::`ps aux | grep command`
<!--SR:!2023-09-14,23,252-->

How to list all the running processes?::`ps -ef`
<!--SR:!2023-10-17,56,272-->

How to display the process details in real time?::`top`
<!--SR:!2023-09-19,28,270-->

How to display info about only the processes owned by a specific user in top?:: Press 'Shift + u' for the prompt. Then enter the username.
<!--SR:!2023-10-20,59,292-->

What is the shortcut key in top to sort the processes according to the memory usage, descending order?::Shift + m
<!--SR:!2023-10-26,65,292-->

What is the shortcut key in top to sort the processes according to the processor utilisation, in descending order?::Shift + p
<!--SR:!2023-10-15,54,272-->

Why jobs started from one terminal are not displayed by the `jobs` command of another terminal?::Because, jobs are handled by the shell in each session. 
<!--SR:!2023-10-26,65,292-->

What is the keyboard shortcut to save the current configuration of top to reuse when top is restarted?::Shift + w
<!--SR:!2023-10-14,53,252-->

How to find the number of CPUs in the system?::`nproc` or `lscpu`
<!--SR:!2023-10-13,52,252-->

How to calculate the maximum load average of a system?::One CPU carry 1.0 max load average. So a system with n CPU has maximum n.0 load average
<!--SR:!2023-10-18,57,272-->
with n CPUs can carry n.0 max load average

What is represented by the load average?::Perceived system load over time
<!--SR:!2023-10-25,64,292-->

How to display the current load average?::`uptime` or `cat /proc/loadavg` or `top` or `w`
<!--SR:!2023-09-15,24,252-->

How to display CPU info?::`lscpu`
<!--SR:!2023-10-17,56,270-->

How to terminate a process inside the top interactive view?::Press `k` for the prompt. Then enter the PID
<!--SR:!2023-10-16,55,272-->

References:
 - [Chapter8, Section1, Listing processes](rh124-rhel8-official-student-workbook.pdf#pageno=262)
 - [Chapter8, Section4, Monitoring process activitiy](rh124-rhel8-official-student-workbook.pdf#pageno=290)
Related:
 - [[Signalling processes]]
 - [[Controlling jobs]]