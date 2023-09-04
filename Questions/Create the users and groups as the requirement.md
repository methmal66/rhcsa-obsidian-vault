---
tags:
  - question
  - rhcsa/rh124/Ch6_Users
reference:
  - "[[Accounts]]"
related:
  - "[[Create a user without a login shell]]"
  - "[[Create a user with uid and password]]"
---
Create the following users and groups memberships: 
- A group named **sysmgrs**
- A user **natasha** who belongs to sysmgrs as a secondary group.
- A user **harry** who also belongs to sysmgrs as a secondary group.
- A user **sarah** who does not have access to an interactive shell on the system
- Natasha, harry, and sarah should all have the password of **redhat**

>[!info]- Answer
>1. `groupadd sysmgrs`
>2. `useradd natasha`
>3. `usermod natasha -aG sysmgrs`
>4. `passwd natasha` and change password to 'redhat'
>5. `useradd harry`
>6. `usermod harry -aG sysmgrs`
>7. `passwd harry` and change password to 'redhat'
>8. `useradd sarah`
>9. `usermod sarah -s /sbin/nologin`

