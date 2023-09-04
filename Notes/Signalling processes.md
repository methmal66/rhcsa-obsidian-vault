---
tags:
  - flashcards
  - rh124/Ch8_Processes
  - rh124
---

How to list all the signals that can be used with kill command to manage background processes?::`kill -l`

<!--SR:!2023-10-27,66,270-->

How to terminate a background process having the PID 1000, without forcing?::`kill 1000` or `kill -15 name` or `kill -SIGTERM 1000`

<!--SR:!2023-10-20,59,288-->

How to forcefully terminate a background process having the PID 1000?::`kill -9 1000` or `kill -SIGKILL 1000`

<!--SR:!2023-10-21,60,288-->

How to terminate the background process having the job number 1?::`kill -SIGTERM %1`

<!--SR:!2023-10-18,57,288-->

How to forcefully suspend(temporary stop) a background process having the PID 1000?::`kill -19 1000` or `kill -SIGSTOP 1000`

<!--SR:!2023-08-25,3,248-->

How to suspend(temporary stop) a background process having the PID 1000?::`kill -20 1000` or `kill -SIGTSTP 1000`

<!--SR:!2023-10-19,58,288-->

How to forcefully continue a stopped background process having the PID 1000?::`kill -18 1000` or `kill -SIGCONT 1000`

<!--SR:!2023-10-24,63,288-->

Why it is advised to use signal names instead of signal numbers?::Because signal numbers may vary on different hardware platforms, but signal names and meanings are standardised.

<!--SR:!2023-10-23,62,288-->

Which command is used to signal all the processes with the given criteria?::`pkill`

<!--SR:!2023-10-16,55,268-->

Which command is used to list all the processes with the given criteria?::`pgrep`

<!--SR:!2023-08-26,4,230-->

How to logout users administratively?::Identify and kill the shell process belong to the user

<!--SR:!2023-08-26,4,282-->
