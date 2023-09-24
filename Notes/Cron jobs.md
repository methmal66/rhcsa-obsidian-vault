---
tags:
  - flashcards
  - rh134/Ch2_Scheduling
  - rh134
  - important
---

Which service is used to handle recurring jobs?::crond

How to edit jobs for the current user?::`crontab -e`

How to list the jobs for current user?::`crontab -l`

How to remove all the jobs of another user by root?::`crontab -r -u amal`

Why the output of a cron job is not displayed in the terminal?::Because cron jobs run in a background environment without an output device (known as a controlling terminal)

What happens to the output of a cron job?::Crond buffers the output and creates an email to send ti to the user specified in the configuration. For system jobs, the email will be sent to the root account.

How to view the format of a cron job?::`cat /etc/crontab`
![500](https://i.imgur.com/Na4Jb9v.png)

What is the crontab record for a job to be executed at 12:15 at 11th of every month and every fridays?::`15 12 11 * Fri my command`

What is the crontab time syntax for a job to be executed at 9AM on February 3rd, every year?::`0 9 3 2 *`

What is the crontab time syntax for a job to be executed every five minutes in between and including 9 a.m. and 4 p.m., but only on each Friday in July?::`*/5 9-16 * jul fri` or `*/5 9-16 * 7 5`

What is the crontab time syntax for a job to be executed every working day (Monday to Friday) two minutes before midnight?::`58 23 * * mon-fri`
