#rhcsa #rhcsa/rh124/Ch11_Logs #flashcards #linux 

Which service stores logging data in a structured, indexed binary file called the journal?::systemd-journald
<!--SR:!2023-08-03,4,284-->

What is the main configuration file of systemd-journald service?::/etc/systemd/journald.conf
<!--SR:!2023-08-03,4,284-->

How to display all log events?::`journalctl`
<!--SR:!2023-08-03,4,284-->

How to display last 10 log events?::`journalctl -n 10`
<!--SR:!2023-08-02,3,250-->

How to display log events in real time?::`journalctl -f`
<!--SR:!2023-07-31,1,230-->

How to display log events with on or above error priority?::`journalctl -p err`
<!--SR:!2023-08-03,4,284-->

How to display log events received today?::`journalctl --since today`
<!--SR:!2023-08-02,3,264-->

How to display log events in the past 10 minutes?::`journalctl --since "10min"`
<!--SR:!2023-08-03,4,284-->

How to display log events received from 2023-06-10 20:30:00 to 2023-07-28 12:00:00?::`journalctl --since "2023-06-10 20:30:00" --until "2023-07-28 12:00:00"`
<!--SR:!2023-08-03,4,278-->

How to display log events with verbose output?::`journalctl -o verbose`
<!--SR:!2023-08-03,4,284-->

What is the use of having a verbose output?::Filtering out complex queries based on hidden field, which are only visible with the verbose output
<!--SR:!2023-08-03,4,284-->

How to query the log events of user with pid=1?::`journalctl _PID=1`
<!--SR:!2023-08-03,4,278-->

Where are the system journals get stored in the volatile storage method by default??::/run/log/journal
What is the default action if the storage parameter is not set in system journals?::auto
<!--SR:!2023-08-03,4,278-->

What defines whether to store system journals in a volatile manner or persistently across reboot?::Storage parameters in journalctl config file
<!--SR:!2023-08-03,4,278-->

Where are the system journals get stored in the persistent storage method?::/var/log/journal
<!--SR:!2023-08-03,4,278-->

How is the system journals get stored in the auto storage method?::If the /var/log/ journal directory exists, then rsyslog uses persistent storage, otherwise it uses volatile storage.
<!--SR:!2023-08-03,4,284-->

What is the advantage of persistent system journal?::Historic data is available immediately after reboot
<!--SR:!2023-08-03,4,270-->

How to display log events until the current boot?::`journalctl -b`
<!--SR:!2023-08-03,4,284-->

How to display log events until the first 3 boot of the system?::`journalctl -b 3`
<!--SR:!2023-08-03,4,270-->

How to display log events limited to last two boots?::`journalctl -b -2`
<!--SR:!2023-08-03,4,278-->

References:
- [Chapter11, Section3, Reviewing system journal entries](rh124-8.0-student-guide.pdf#pageno=388)
- [Chapter11, Section4, Preserving the system journal](rh124-8.0-student-guide.pdf#pageno=397)
Related:
- [[Syslog files]]