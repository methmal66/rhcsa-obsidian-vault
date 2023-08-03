#linux #flashcards #rhcsa #rhcsa/rh124/Ch8_Processes 

What is a process?::A program in execution

What is a job?::A process interactively started by a user and doesn't detach

What is a task?::

What is a thread?::

What is a core?::

What does it mean that a process is running?::Its either executing in the CPU or waiting for that

What does it mean that a process is sleeping?::Its waiting without running, until some conditions to satisfy 

What does it mean that a process is stopped?::Its being stopped from executing by a user or kernel

What does it mean that a process is in the zombie state?::It has signalled its parent as it exits. All resources except for the process identity (PID) are released.

What are the only process states which are considered when calculating the load average?::Running and Sleeping states

What is the process state that will be never observed in process-listening utilities?::Zombie state

Which process state is represented by the flag 'R'?::Running state

Which process state is represented by the flags 'S, D, K, I'?::Sleeping state

Which process state is represented by the flag 'T'?::Stop state

Which process state is represented by the flag 'Z, X'?::Zombie state

How to display the current process details one time?::`ps aux`

How to display the current details of processes with the given command?::`ps aux | grep command`

How to list all the running processes?::`ps -ef`

How to display the process details in real time?::`top`

How to display info about only the processes owned by a specific user in top?:: Press 'Shift + u' for the prompt. Then enter the username.

What is the shortcut key in top to sort the processes according to the memory usage, descending order?::Shift + m

What is the shortcut key in top to sort the processes according to the processor utilisation, in descending order?::Shift + p

Why jobs started from one terminal are not displayed by the `jobs` command of another terminal?::Because, jobs are handled by the shell in each session. 

What is the keyboard shortcut to save the current configuration of top to reuse when top is restarted?::Shift + w

How to find the number of CPUs in the system?::`nproc`

How to calculate the maximum load average of a system?::One CPU carry 1.0 max load average. So a system 
with n CPUs can carry n.0 max load average

What is represented by the load average?::Perceived system load over time

How to display the current load average?::`uptime` or `cat /proc/loadavg` or `top` or `w`

How to display CPU info?::`lscpu`

How to terminate a process inside the top interactive view?::Press `k` for the prompt. Then enter the PID

References:
 - [Chapter8, Section1, Listing processes](rh124-8.0-student-guide.pdf#pageno=262)
 - [Chapter8, Section4, Monitoring process activitiy](rh124-8.0-student-guide.pdf#pageno=290)
Related:
 - [[Signalling processes]]
 - [[Controlling jobs]]