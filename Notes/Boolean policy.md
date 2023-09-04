---
tags:
  - linux
  - rhcsa
  - flashcards
  - rhcsa/rh134/Ch4_SELinux
related:
  - "[[Context policy]]"
  - "[[Enforcement mode]]"
  - "[[Troubleshoot SELinux]]"
---
Why SELinux boolean policies are used for?::To turn on or off an application specific behaviour

How to list all the available boolean policies?
?
`getsebool -a`
![300](https://i.imgur.com/Z6cbWqx.png)


How to display the state of a single boolean policy
?
`getsebool httpd_enable_homedirs`
![300](https://i.imgur.com/U6osE6Q.png)

How to temporary set a SELinux boolean policy?::`setsebool httpd_enable_homedirs on`

How to permanently set a SELinux boolean policy?::`setsebool -P httpd_enable_homedirs on`

