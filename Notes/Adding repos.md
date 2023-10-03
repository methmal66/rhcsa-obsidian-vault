---
tags:
  - flashcards
  - rh124/Ch13_software
  - rh124
  - important
---
>[!faq] How to add a new repo to the system?::`dnf config-manager --add-repo "your repo url here"`

>[!faq] How to enable(or disable) an already available repo?::`dnf config-manager --enable your-repo-name`

>[!faq] How to list all the available repos?::`dnf repolist all`

All dnf commands works similar to yum commands

What is a repo (repository) ?
	A central storage for store and receive packages

What does software providers use to digitally sign a RPM package?::GPG key

What happens when a GPG key does not match?::RPM system refuse to install the package
