---
tags:
  - linux
  - rhcsa
  - flashcards
  - rhcsa/rh134/Ch4_SELinux
related:
  - "[[Boolean policy]]"
  - "[[Enforcement mode]]"
  - "[[Troubleshoot SELinux]]"
---
What is the SELinux label belongs to every resource entity, such as a file, process, directory, or port is called?
?
Context label
![](https://i.imgur.com/JO88ZUe.png)

What does a context label mapped into?::A defined SELinux policy rule

How to list files with SELinux label?
?
`ls -Z /var/www`
![](https://i.imgur.com/CHU5AiN.png)

How to list processes with SELinux label?
?
`ps axZ`
![](https://i.imgur.com/mU0HpSW.png)

What label get assigned to a files that doesn't match with an existing SELinux policy?::The file inherits the same label from it's parent directory

When files are labeled with a correct SELinux context?::Files are created in default locations that have an existing labeling policy, or a policy
exists for a custom location.

When the inherited label might not be correct for the new file's intended purpose?::A file is created in an unexpected location without an existing labeling policy

What happens to the context label of a file when the file is copied using cp command?::File get assigned with a context label inherited form the new location, because new inode is created

What happens to the context label of a file when the file is moved using mv command?::Context label does not change, because the same inode is used

How to temporary set the label of a file?::`chcon -t httpd_sys_content /virtual`

How to restore the temporary labels to their default values?::`restorecon /virtual`

How to list all the default SELinux file contexts?
?
`semanage fcontext -l`
![](https://i.imgur.com/3IlJ0Qw.png)

How to add a SELinux file context policy to a directory?
?
`semanage fcontext -at httpd_sys_content_t /virtual
`restorecon /virtual`

How to view any local customisations to the default policy?
?
`semanage fcontext -lC`
![](https://i.imgur.com/FUphnVN.png)




