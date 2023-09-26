---
tags:
  - flashcards
  - "#rh134"
  - rh134/Ch7_NetStorage
---
Why the automounter function was created?::To solve the problem that unprivileged users dont have sufficient permissions to use mount command, so they cannot access removable devices

Why automounter mounts on-demand, not permanently?::For security; To protect the filesystems from unexpected corruptions and to stop server getting infected.

What automounter do when there are redundant paths or servers?::Select the fastest connection

When does automounter mount shared directories?::Immediately when the files are accessed, and remain mounted while the directory is in use.

When does automounter unmount a shared directory?::Each time it is in no use, has no open file or files not being used by a processor.

Which commands are used by the automounter?::mount and umount

What are the steps to setup automounter in a client machine?
?
1. Install required packages `dnf install autofs`
2. Write the two config files
3. Restart the automounter `systemctl restart autofs`

How to write config files to mount servera:/internal on /remote/internal and servera:/external on /remote/external?
?
`echo "/remote  /etc/auto.main" >> /etc/auto.master.d/master.autofs`
`echo "internal  -rw   servera:/internal" >> /etc/auto.main`
`echo "external  -rw  servera:/external" >>> /etc/auto.main`

How to verify if a remote filesystem is mounted?::
?
`df -h`
![](https://i.imgur.com/ao6txri.png)
