---
tags:
  - interview
references:
  - https://youtu.be/b-m0Oz_8W3k?si=ZycWexBOHTyEpc55&t=1178
  - "[[Installing packages]]"
---
Lets assume, we want to undo the installation of httpd package.
1. `dnf history`
2. `dnf history info 8` (8 is the transaction no)
3. `dnf history undo 8`