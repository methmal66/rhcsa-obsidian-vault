---
tags:
  - flashcards
  - rh134
  - rh134/Ch7_NetStorage
aliases:
  - NFS
related:
  - "[[Attach new partitions]]"
  - "[[Automounter]]"
references:
  - https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/security_guide/sect-security_guide-securing_nfs-do_not_use_the_no_root_squash_option
  - https://serverfault.com/a/611013
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

How to add records into /etc/exports config file which will share the directories?
?
![](https://i.imgur.com/beLwGKh.png)
ro - Read only
rw - Read and write (full permission)

How to allow nfs from the firewall?
?
`firewall-cmd --add-service=nfs --permanent`
`firewall-cmd --add-service=rpc-bind --permanent`

What is the extra step needed to give write access to the shared folder?
?
Grand write access to user "nobody" in nfs server to the selected files
`setfacl -m u:nobody:rwx /sharenfs`

How to list all the directories shared by a particular server?
?
`showmount -e server`

How to temporarily mount a shared directory inside a client machine?::`mount server:/share /mnt`
