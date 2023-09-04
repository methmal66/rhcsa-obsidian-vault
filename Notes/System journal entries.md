---
tags:
  - flashcards
  - rh124/Ch11_Logs
  - rh124
---

Which service stores logging data in a structured, indexed binary file called the journal?::systemd-journald

<!--SR:!2023-08-25,21,304-->

What is the main configuration file of systemd-journald service?::/etc/systemd/journald.conf

<!--SR:!2023-08-21,17,304-->

How to display all log events?::`journalctl`

<!--SR:!2023-08-24,20,304-->

How to display last 10 log events?::`journalctl -n 10`

<!--SR:!2023-08-14,10,250-->

How to display log events in real time?::`journalctl -f`

<!--SR:!2023-08-20,16,250-->

How to display log events with on or above error priority?::`journalctl -p err`

<!--SR:!2023-08-27,23,304-->

How to display log events received today?::`journalctl --since today`

<!--SR:!2023-08-20,16,284-->

How to display log events in the past 10 minutes?::`journalctl --since "10min"`

<!--SR:!2023-08-26,22,304-->

How to display log events received from 2023-06-10 20:30:00 to 2023-07-28 12:00:00?::`journalctl --since "2023-06-10 20:30:00" --until "2023-07-28 12:00:00"`

<!--SR:!2023-08-19,15,278-->

How to display log events with verbose output?::`journalctl -o verbose`

<!--SR:!2023-08-19,15,284-->

What is the use of having a verbose output?::Find hidden fields to include

<!--SR:!2023-08-25,21,304-->

How to query the log events of user with pid=1?::`journalctl _PID=1`

<!--SR:!2023-08-22,18,298-->

Where are the system journals get stored in the volatile storage method by default??::/run/log/journal

<!--SR:!2023-08-08,4,296-->

What is the default action if the storage parameter is not set in system journals?::auto

<!--SR:!2023-08-21,17,298-->

What defines whether to store system journals in a volatile manner or persistently across reboot?::Storage parameters in journalctl config file

<!--SR:!2023-08-06,2,258-->

Where are the system journals get stored in the persistent storage method?::/var/log/journal

<!--SR:!2023-08-23,19,298-->

How is the system journals get stored in the auto storage method?::If the /var/log/ journal directory exists, then persistent storage is used, otherwise it uses volatile storage.

<!--SR:!2023-08-26,22,304-->

What is the advantage of persistent system journal?::Historic data is available immediately after reboot

<!--SR:!2023-08-18,14,270-->

How to display log events until the current boot?::`journalctl -b`

<!--SR:!2023-08-27,23,304-->

How to display log events until the first 3 boot of the system?::`journalctl -b 3`

<!--SR:!2023-08-24,20,290-->

How to display log events limited to last two boots, under the persistent storage method?::`journalctl -b -2`

<!--SR:!2023-08-19,15,278-->
