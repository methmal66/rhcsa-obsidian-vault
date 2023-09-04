---
tags:
  - rhcsa
  - linux
  - flashcards
  - rhcsa/rh134/Ch4_SELinux
related:
  - "[[Enforcement mode]]"
  - "[[Context policy]]"
  - "[[Boolean policy]]"
---
What is the most common SELinux issue?::An incorrect context on new, copied, or moved files

What should be done in the first step, to troubleshoot a failing service, which is known to have a working SELinux policy?::Check the service's 'se_linux' man page to verify the correct context type label. View the affected process and file attributes to verify that the correct labels are set.

Which package provides the tools to troubleshoot SELinux related issues?::setroubleshoot-server

Which log file used by SELinux to log action denials?::/var/log/audit/audit.log

