#linux #flashcards #rhcsa #rhcsa/rh124/Ch8_Processes 

How to list all the signals that can be used with kill command to manage background processes?::`kill -l`

How to terminate a background process having the PID 1000, without forcing?::`kill 1000` or `kill -15 name` or `kill -SIGTERM 1000` 

How to forcefully terminate a background process having the PID 1000?::`kill -9 1000` or `kill -SIGKILL 1000`

How to terminate the background process having the job number 1?::`kill -SIGTERM %1`

How to forcefully suspend(temporary stop) a background process  having the PID 1000?::`kill -19 1000` or `kill -SIGSTOP 1000`

How to suspend(temporary stop) a background process having the PID 1000?::`kill -20 1000` or `kill -SIGTSTP 1000`

How to forcefully continue a stopped background process having the PID 1000?::`kill -18 1000` or `kill -SIGCONT 1000`

Why it is advised to use signal names instead of signal numbers?::Because signal numbers may vary on different hardware platforms, but signal names and meanings are standardised.

How to terminate without force, multiple processes based on the command pattern?::`killall command`

How to terminate without force, all the processes own by a given user?::`pkill -U user`

How to list all the processes with PIDs belong to a user?::`pgrep -lu user`

How to logout users administratively?::Terminate all the processes belong to that user with `pkill -SIGTERM -U user`

References:
 - [Chapter8, Section3, Killing processes](rh124-8.0-student-guide.pdf#pageno=262)
Related:
 - [[Monitoring Processes]]
 - [[Controlling jobs]]