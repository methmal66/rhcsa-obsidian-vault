---
tags:
  - flashcards
  - rh124/Ch10_SSH
  - rh124
related:
  - "[[Accounts]]"
  - "[[Remote file transferring]]"
---

How SSH encrypt password based connections, thought they don't have a key pair?::Using symmetric encryption

<!--SR:!2023-08-26,22,307-->

Why it is not recommended to authenticate using passwords?::Passwords can be vulnerable to brute-force attacks, phishing attempts, and other password-based attacks

<!--SR:!2023-08-23,19,296-->

In which format passwords transmitted to the server, in password based authentication?::In encrypted format

<!--SR:!2023-08-21,17,307-->

What is the most secure method to authenticate users with ssh?::Key based authentication

<!--SR:!2023-08-08,4,306-->

# Step1: Generate a ssh key pair

How to generate a new key pair for a user?
?
![500](https://i.imgur.com/cTx5PBW.png)

<!--SR:!2023-08-25,21,307-->

What is the purpose of using a private key?::Decode the packets after receiving

<!--SR:!2023-08-24,20,307-->

Who can view the private key?::Only the server which generated the key. It is not shared.

<!--SR:!2023-08-22,18,276-->

What is the purpose of using a public key?::Encode the packets before sending

<!--SR:!2023-08-27,23,307-->

Who can view the public key?::Any host can view it. It is shared.

<!--SR:!2023-08-24,20,307-->

# Step2: Copy the public key to the server

How to configure the client's public key in remote server?:: It should be copied to the server manually or using tools

<!--SR:!2023-08-26,22,307-->

What happens when a client's public key is manually copied to a server?::It is inserted into server's `~/.ssh/authorized_keys` and server

<!--SR:!2023-08-19,15,287-->

How to configure the remote server's public key in client host?::It is automatically copied to known_hosts file during the first connection between the hosts

<!--SR:!2023-08-20,21,290-->

How to copy our public key into a remote user using ssh?
?
![600](https://i.imgur.com/98wIjUR.png)

<!--SR:!2023-08-23,19,296-->

Why do you get to confirm a ssh connection only during the first time interacting with the server?::Because our client does not recognise the server until that point.

<!--SR:!2023-08-08,4,292-->

How to copy the ssh key when you using a cloud instance so that, they dont provide you any user password?::Use cloud console to upload the keys

<!--SR:!2023-08-08,4,292-->

Which type of SSH hosts maintaining a known_hosts file?::Client hosts

<!--SR:!2023-08-19,20,290-->

Which type of SSH hosts maintaining a authorized_keys file?::Server hosts

<!--SR:!2023-08-22,18,296-->

What is get inserted into `~/.ssh/known_hosts`?
?
Host keys of those hosts each regular user has connected with before or shared keys with
![400](https://i.imgur.com/HPX8Hku.png)

<!--SR:!2023-08-08,4,306-->

Where are host keys stored?
?
`/etc/ssh`
![400](https://i.imgur.com/WWSn7cV.png)

<!--SR:!2023-08-07,3,272-->

Which type of hosts maintain a `~/.ssh/known_hosts`?::Hosts which use SSH client

<!--SR:!2023-08-08,4,304-->

What is get inserted into `/etc/ssh/sshd_known_hosts`?::Hosts configured by sysadmin for all users

<!--SR:!2023-08-08,4,306-->

What is get inserted into `~/.ssh/authorized_keys`?
?
Public keys of those users who are authorised to establish a ssh connection with the server
![500](https://i.imgur.com/5hPyeRN.png)

<!--SR:!2023-08-08,4,292-->

Why it is a malpractices to edit known_host file?::Clients can confuse the sever with a man in the middle attack

<!--SR:!2023-08-08,4,292-->

# Step3: Test the ssh connection

Which users can connect to a server using ssh?::Only users whose public key is in the server's `~/.ssh/authorized_keys`

<!--SR:!2023-08-25,21,307-->

How to login to a remote session?
?
![500](https://i.imgur.com/TWWKv9s.png)

<!--SR:!2023-08-08,4,292-->

How to execute a command in a remote server without interactively login to it
ssh?
?
`ssh -i ~/ssh/id_bimal_serverb bimal@serverb "command to execute"`

<!--SR:!2023-08-08,4,306-->

How to list all the users logged in to a server?
?
![500](https://i.imgur.com/syNft4c.png)

<!--SR:!2023-08-08,4,306-->

<!--SR:!2023-08-03,4,287-->

# Step4: Setup config file

To make it further easier, edit the ssh client config file (~/.ssh/config) and add the below lines
What are the configurations needed to add in the `~/.ssh/config` in order to create a ssh alias
?
![300](https://i.imgur.com/VQhNHKY.png)

<!--SR:!2023-08-08,4,306-->

How to login to a remote server using a ssh alias?
?
![500](https://i.imgur.com/lFp8p4u.png)

<!--SR:!2023-08-08,4,292-->

# Step5: Customise service configurations

Which file should be edited to enhance the security of the ssh server?
?
`/etc/ssh/sshd_config` and
`/etc/ssh/ssh_config`

<!--SR:!2023-08-08,4,304-->

If you have configured a regular user with key authentication, you can enhance the security by editing the below options.

1. To disable root login, set `PermitRootLogin` to `no`
2. To disable password authentication for every user, set `PasswordAuthentication` to `no`

Then reload the sshd service to changes to get affect

```
systemctl reload sshd
```
