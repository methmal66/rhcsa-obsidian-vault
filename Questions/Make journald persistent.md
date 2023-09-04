---
tags:
  - question
  - rh124/Ch11_Logs
reference:
  - "[[System journal entries]]"
---

Configure **journald** to persist between reboots

> [!info]- Answer
>
> 1.  `/etc/systemd/journald.conf` and make it `Storage=persistent`
>     (`man journald.conf` to get help)
