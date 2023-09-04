---
tags:
  - question
  - rh124/Ch3_File-basics
reference:
  - "[[Copying files]]"
  - "[[Output redirecting]]"
related:
  - "[[List files containing a pattern]]"
  - "[[Find and copy files]]"
---

Find all lines in the file **/usr/share/dict/words** that contain the string **seismic**. Put a copy of all these lines in their original order in the file **/root/wordlist**. /root/wordlist should contain no empty lines and all lines must be exact copies of the original lines in /usr/share/dict/words.

> [!info]- Answer
>
> 1.  `cat /usr/share/dict/words | grep seismic >> /rot/wordlist`
