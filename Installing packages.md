#linux #flashcards #rhcsa #rhcsa/rh124/Ch13_software 

In which form all the software on Redhat system is provided?::As a RPM package

What is the file extension for a RPM package?::.rpm

How to install a package using rpm?::`rpm -ivh package-name.rpm`

When is it advised to exact and inspect rpm files before installing?::To find any possible vulnerabilities in third party packages

What is the advantage of using dnf to install packages over yum?::dnf is fast, modern and uses less memory

How to search for a installed or available packages from the name
?
![500](https://i.imgur.com/gc8f0DH.png)

How to search for a installed or available packages from name, description and summary
?
![500](https://i.imgur.com/6B2tH79.png)

How to install a latest version of a package
?
![500](https://i.imgur.com/k1PkO90.png)

How to download a package without installing it?::`dnf install --downloadonly pkg`

How to update the entire system, every package installed in the system?::`dnf update`

How to remove a package?::`dnf remove pkg`

How to list all the available group installations?
?
![250](https://i.imgur.com/7mPR9fp.png)

How to find info about a group?
?
![400](https://i.imgur.com/Cn99zzv.png)

How to install a group of packages?::`dnf group install "Server with GUI`

How to see yum history?
?
![400](https://i.imgur.com/WqHHCTL.png)

How to display info about a previous transaction which has the given transaction id?
?
![500](https://i.imgur.com/inJe2Le.png)

How to undo a previous transaction which has the given transaction id?
?
`yum history undo 5`
![500](https://i.imgur.com/X0Rusoj.png)


What is a module?::Set of packages related to a single application

What is a module profile?:: Organisation of a module, where recommended packages are installed together for a particular use case, such as a server, client, development, minimal install, or other

Why modules are not used nowadays?::Because containers have replaced modules

What happens when updating a package?::Removing the older version and installing the newer version 

Why different versions of kernel is installed in the same system?::Since a new kernel can only be tested by booting to that kernel, If the new kernel fails to boot, the old kernel is still available and bootable.

References:
- [Chapter13, Section3, Installing and updating software packages with yum](rh124-8.0-student-guide.pdf#pageno=502)
- [Chapter13, Section5, Managing package module streams](rh124-8.0-student-guide.pdf#pageno=523)
Related:
- [[rpm file name]]
- [[rpm file content]]
- [[Adding repos]]
