---
tags:
  - question
  - rhcsa/rh124/Ch3_File-basics
reference:
  - "[[Copying files]]"
related:
  - "[[List files containing a pattern]]"
  - "[[Copy lines containing a pattern]]"
---
Find out files owned by jack and copy them to directory /root/findresults

>[!faq]- Answer 1
>1. `mkdir /root/findresults`
>2. `for file in $(find / -user jack); do; cp $file /root/findresults; done`

