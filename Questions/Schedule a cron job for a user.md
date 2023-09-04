---
tags:
  - question
  - rhcsa/rh134/Ch2_Scheduling
reference:
  - "[[Recurring cron jobs]]"
---
User **natasha** must configure a cron job, local time **14:23** runs and executes: `/bin/echo hiya` every day.

>[!Info]- Answer
>1. `crontab –eu natasha`  then add `23 14/bin/echo hiya` to the file
>2. `crontab -lu natasha` and verify thechanges


