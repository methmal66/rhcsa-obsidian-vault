---
tags:
  - flashcards
  - rh124/Ch13_software
  - rh124
---

In which form all the software on Redhat system is provided?::As a RPM package

<!--SR:!2023-08-08,4,270-->

What is the file extension for a RPM package?::.rpm

<!--SR:!2023-08-08,4,270-->

How to install a package using rpm?::`rpm -ivh package-name.rpm`

<!--SR:!2023-08-08,4,270-->

When is it advised to exact and inspect rpm files before installing?::To find any possible vulnerabilities in third party packages

<!--SR:!2023-08-08,4,270-->

What is the advantage of using dnf to install packages over yum?::dnf is fast, modern and uses less memory

<!--SR:!2023-08-08,4,270-->

How to search for a installed or available packages from the name
?
![500](https://i.imgur.com/gc8f0DH.png)

<!--SR:!2023-08-08,4,270-->

How to search for a installed or available packages from name, description and summary
?
![500](https://i.imgur.com/6B2tH79.png)

<!--SR:!2023-08-08,4,270-->

How to install a latest version of a package
?
![500](https://i.imgur.com/k1PkO90.png)

<!--SR:!2023-08-08,4,270-->

How to download a package without installing it?::`dnf install --downloadonly pkg`

<!--SR:!2023-08-08,4,270-->

How to update the entire system, every package installed in the system?::`dnf update`

<!--SR:!2023-08-08,4,270-->

How to remove a package?::`dnf remove pkg`

<!--SR:!2023-08-07,3,250-->

How to list all the available group installations?
?
![250](https://i.imgur.com/7mPR9fp.png)

<!--SR:!2023-08-07,3,250-->

How to find info about a group?
?
![400](https://i.imgur.com/Cn99zzv.png)

<!--SR:!2023-08-08,4,270-->

How to install a group of packages?::`dnf group install "Server with GUI`

<!--SR:!2023-08-08,4,270-->

How to see dnf history?
?
![400](https://i.imgur.com/WqHHCTL.png)

How to display info about a previous transaction which has the given transaction id?
?
![500](https://i.imgur.com/inJe2Le.png)

How to undo a previous transaction which has the given transaction id?
?
`yum history undo 5`
![500](https://i.imgur.com/X0Rusoj.png)

<!--SR:!2023-08-08,4,270-->

What is a module?::Set of packages related to a single application

<!--SR:!2023-08-08,4,270-->

What is a module profile?:: Organisation of a module, where recommended packages are installed together for a particular use case, such as a server, client, development, minimal install, or other

<!--SR:!2023-08-08,4,270-->

Why modules are not used nowadays?::Because containers have replaced modules

<!--SR:!2023-08-08,4,270-->

What happens when updating a package?::Removing the older version and installing the newer version

<!--SR:!2023-08-08,4,270-->

Why different versions of kernel is installed in the same system?::Since a new kernel can only be tested by booting to that kernel, If the new kernel fails to boot, the old kernel is still available and bootable.

<!--SR:!2023-08-08,4,270-->
