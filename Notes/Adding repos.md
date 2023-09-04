---
tags:
  - flashcards
  - rh124/Ch13_software
  - rh124
---

All dnf commands works similar to yum commands

What is a repo (repository) ?::A central storage for store and receive packages

<!--SR:!2023-08-08,4,270-->

How to add a new repo to the system?::`dnf config-manager --add-repo "your repo url here"`

<!--SR:!2023-08-07,3,250-->

How to enable(or disable) an already available repo?::`dnf config-manager --enable your-repo-name`

<!--SR:!2023-08-08,4,270-->

What does software providers use to digitally sign a RPM package?::GPG key

<!--SR:!2023-08-08,4,270-->

What happens when a GPG key does not match?::RPM system refuse to install the package

<!--SR:!2023-08-08,4,270-->

How to list all the available repos
?
![500](https://i.imgur.com/Wn3oy78.png)

<!--SR:!2023-08-07,3,250-->
