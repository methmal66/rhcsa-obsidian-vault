---
tags:
  - flashcards
  - rh124/Ch6_Users
  - rh124
---

What is the cause to mismatching uid and gid of a regular user?::Creating a regular group without a higher gid

<!--SR:!2023-08-10,4,270-->

What is the problem of having different uid and gid for a regular user?::It is confusing to work with users and groups

<!--SR:!2023-08-10,4,270-->

How to create a group with higher an higher id?::`groupadd -g 5000 mygroup`

<!--SR:!2023-08-10,4,270-->
