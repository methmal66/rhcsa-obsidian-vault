#linux #rhcsa #rhcsa/rh124/Ch13_software #flashcards 

All dnf commands works similar to yum commands

What is a repo (repository) ?::A central storage for store and receive packages

How to add a new repo to the system?::`dnf config-manager --add-repo "your repo url here"`

How to enable(or disable) an already available repo?::`dnf config-manager --enable your-repo-name`

What does software providers use to digitally sign a RPM package?::GPG key

What happens when a GPG key does not match?::RPM system refuse to install the package

How to list all the available repos
?
![500](https://i.imgur.com/Wn3oy78.png)

References:
- [Chapter13, Section4, Enabling Yum Software repositories](rh124-8.0-student-guide.pdf#pageno=534)
Related:
- [[Redhat subscription]]
- [[Installing packages]]