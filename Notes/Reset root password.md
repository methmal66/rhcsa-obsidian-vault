---
tags:
  - rh134
  - rh134/Ch8_Boot
  - important
  - flashcards
related:
  - "[[Kernel parameters]]"
---
What are the steps to reset the root password when the system is physically accessible?
?
1. Access the initramfs debug shell by giving `rd.break` as a kernel parameter
2. Remount the filesystem `mount -o remount,rw /sysroot`
3. Switch into a chroot jail `chroot /sysroot`
4. Set a new root password `passwd root`
5. Enable auto relabelling `touch /.autorelabel`
6. Login as rot using the new password

What is the impact of providing the kernel parameter?::The system breaks just before hands control from the initramfs to the systemd

Where does the actual root filesystem get mounted during the root shell?::/sysroot

What is the reason to enable auto relabelling?::To make sure that al unlabelled files, including /etc/ shadow at this point, get relabelled during boot.

