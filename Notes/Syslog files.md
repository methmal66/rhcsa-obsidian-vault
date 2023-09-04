---
tags:
  - flashcards
  - rh124/Ch11_Logs
  - rh124
---

Why processes and kernel record a log of events that happen?::To audit the system and troubleshoot the problems

<!--SR:!2023-08-22,18,290-->

What is the default directory of log files, which is persist across reboots?::/var/log

<!--SR:!2023-08-24,20,304-->

Which service is the core of the system's event logging architecture?::systemd-journald

<!--SR:!2023-08-22,18,290-->

Which service reads the syslog messages from systemd-journal which are from multiple sources, sorts them and write persistently in to files as human readable format?::rsyslog

<!--SR:!2023-08-27,23,304-->

What is the log file where most of the syslog messages are written into?::/var/log/messages

<!--SR:!2023-08-22,18,290-->

What is the log file which store messages related to security and authentiction?::/var/log/secure

<!--SR:!2023-08-21,17,298-->

What is the log file which store messages related to mail server?::/var/log/maillog

<!--SR:!2023-08-25,21,304-->

What is the log file which stores the messages related to scheduled job execution?::/var/log/cron

<!--SR:!2023-08-23,19,290-->

What is the log file which stores the messages related to system startup?::/var/log/boot.log

<!--SR:!2023-08-26,22,304-->

Which best use case for using journalctl?::To view and analyse logs with complex queries

<!--SR:!2023-08-26,22,304-->

Which is the best use case for using manual log files?::To store logs into different locations and backup them separately

<!--SR:!2023-08-27,23,304-->

What is the highest log priority?::emerg (0)

<!--SR:!2023-08-23,19,290-->

Which priority logs are used during an emergency situation where a system is unusable?::emerg (0)

<!--SR:!2023-08-22,18,290-->

Which log priority is used when there is an action to be taken immediately?::alert (1)

<!--SR:!2023-08-19,15,284-->

Which log priority is used when the system is in a critical condition?::crit (2)

<!--SR:!2023-08-27,23,304-->

Which log priority is used when there are non critical errors?::err (3)

<!--SR:!2023-08-25,21,298-->

Which log priority is used when there are warning conditions?::warning (4)

<!--SR:!2023-08-23,19,290-->

Which log priority is used when there are normal but significant event?::notice (5)

<!--SR:!2023-08-06,2,250-->

Which log priority is used to store informational events?::info (6)

<!--SR:!2023-08-06,2,264-->

Which log priority is used to store debugging level message?::debug (7)

<!--SR:!2023-08-23,19,290-->

What is the lowest log priority?::debug (7)

<!--SR:!2023-08-25,21,304-->

Which properties of log messages are used by rsyslog service to determine how to handle the log messages?::Facility(service) and priority

<!--SR:!2023-08-17,13,264-->

What is the default configuration file of rsyslog?::/etc/rsyslog.conf

<!--SR:!2023-08-24,20,304-->

What directory is dedicated for software packages to configure custom rules to handle log messages?::/etc/rsyslog.d

<!--SR:!2023-08-20,16,250-->

Which character is used to indicate all log priorities in rsyslog config files?:: "\*" Astrix

<!--SR:!2023-08-21,17,304-->

What is the special keyword that can be used instead of a log priority, to indicate that no messages from that particular service should be stored in the given file?::none

<!--SR:!2023-08-21,17,298-->

Why emergency log messages are directly displayed in the terminal, instead of storing in a log file?::Because they are time critical

<!--SR:!2023-08-24,20,290-->

Why logrotate is being used?::To keep log files from taking too much space and delete them after a certain period

<!--SR:!2023-08-19,15,250-->

How to manually send a log message to user facility with debug priority?::`logger -p user.debug "This is a debug message"`

<!--SR:!2023-08-20,16,278-->
