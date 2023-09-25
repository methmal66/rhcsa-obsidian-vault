---
tags:
  - flashcards
  - rh134
  - rh134/Ch7_NetStorage
aliases:
  - NFS
related:
  - "[[Attach new partitions]]"
---
What is the use of NFS?::To use a remote file system over the network, as its located in our local machine

What are the steps of configuring a nfs server?
?
1. Having filesystem mounted and ready to be shared
2. Install the necessary packages
3. Add records to the config file
4. Enable the required services
5. Allow the service from the firewall
6. Start the serice

How to install and enable the service?
?
`dnf install nfs-utils`
`systemctl enable --now nfs-server`

Which config file is used to add records about the sharing directories?::`/etc/exports`

What are the sample records you can add to /etc/exports?
?
Full access - rw
Read only - ro

How to allow nfs from the firewall?
?
`firewall-cmd --add-service=nfs --permanent`
`firewall-cmd --add-service=rpc-bind --permanent`

How to list all the directories shared by a particular server?
?
`showmount -e server`

How to mount a shared directory inside a client machine?::`mount server:/share /mnt`

