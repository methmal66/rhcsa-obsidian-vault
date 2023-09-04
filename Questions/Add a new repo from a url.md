---
tags:
  - question
  - rhcsa/rh124/Ch13_software
reference:
  - "[[Adding repos]]"
---
A YUM source has been provided in the http://instructor.example.com/pub/rhel6/dvd. Configure your system to make it use normally.

>[!info]- Answer
>1. `vim /etc/yum.repos.d/base.repo` and add the below lines
>```
>[base]
>name=base
>baseurl=http://instructor.example.com/pub/rhel6/dvd
>enabled=1
>gpgcheck=false
>```
>2. `dnf repolist` and verify is the above repo show up

