---
tags:
  - question
  - rhcsa/rh124/Ch6_Users
reference:
  - "[[Accounts]]"
related:
  - "[[Create a user without a login shell]]"
  - "[[Create the users and groups as the requirement]]"
---
Create a user named **alex**, and the user id should be **1234**, and the password should be **alex111**.

>[!note]- Answer
>1. `useradd alex -u 1234`
>2. `passwd alex` then change the password into 'alex111'