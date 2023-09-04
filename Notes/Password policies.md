#rhcsa #rhcsa/rh124/Ch6_Users #flashcards #linux

![](https://i.imgur.com/WW5homN.png)

Who become the default owner of the file?::`User who created the file`
<!--SR:!2023-08-15,24,306-->

Who can delete a file or directory?::Root, owner or anyone with the write access to the parent directory
<!--SR:!2023-10-17,72,291-->

What is the recommended method of preventing an account from accessing by an employee who has left the company?::Lock the account
<!--SR:!2023-08-16,25,311-->

What happens when a user account is locked?::User cannot login to the account, until administrator unlock it
<!--SR:!2023-08-17,26,311-->

How to lock a user account?::`usermod -L username`
<!--SR:!2023-08-15,24,311-->

How to unlock a user account?::`usermod -U username`
<!--SR:!2023-10-02,57,291-->

Which file is used to configure default values for user's password aging policies
?
/etc/login.defs
![300](https://i.imgur.com/fVQkUon.png)
<!--SR:!2023-10-01,56,284-->

Which file is used to configure the password policies of each user
?
/etc/shadow
![600](https://i.imgur.com/JI8NPqH.png)
<!--SR:!2023-08-17,26,306-->

How to enforce a user to change their password immediately on the next login?::`change -d 0 username`
<!--SR:!2023-08-14,23,311-->

What happens when a password is expired?::It will be forcefully prompt the user to reset the password
<!--SR:!2023-08-16,25,304-->

How to display all the password aging policies of a user
?
![400](https://i.imgur.com/xKNXo3E.png)
<!--SR:!2023-08-17,26,308-->

How to expire a password in future?::`chage -E 2023-08-10 username`
<!--SR:!2023-08-18,27,311-->

How to make password possible to be changed any time before it get expired?::`chage -m 0 usename` 
<!--SR:!2023-08-10,19,288-->

Which value is used to set the date parameters of the `chage` command as "never"?::-1
<!--SR:!2023-08-13,22,306-->

What is the purpose of having a max days for passwords?::To give the users freedom to reset their password at anytime they like, within the given period
<!--SR:!2023-08-14,23,305-->

What is the reason to password get expired?::User haven't reset the password before the date specified by the max days.
<!--SR:!2023-08-15,24,308-->

What is the reason to password become inactive?::User haven't reset the password at all, even after password get expired.
<!--SR:!2023-08-18,27,306-->

What is the purpose of having a min days for passwords?::To avoid users from resetting their password for a specific number of days after the last password change date
<!--SR:!2023-08-12,21,308-->

How to prevent any user from resetting their passwords?::`chmod u-s $(which passwd)`
<!--SR:!2023-08-09,3,270-->

References:
- [Chapter6, Section5 Managing User Passwords](rh124-rhel8-official-student-workbook.pdf#pageno=193)
Related:
- [[Accounts]]