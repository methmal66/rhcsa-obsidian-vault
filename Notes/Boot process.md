---
tags:
  - rh134
  - rh134/Ch8_Boot
  - flashcards
---
What is the system firmware used in older machines?::BIOS (Basic Input Output Systems)

What is the system firmware used in modern machines?::UEIF (Unified Extensible Firmware Interface)

What is the purpose of running the POST (Power On Self Test)?::To check if all the hardware components are working properly.

How the bootable device is found in BIOS machines?
?
BIOS looks the last two bytes of the first sector of each disk to find a valid boot signature. 
![400](https://i.imgur.com/wOFRn4r.png)

How does BIOS find the boot loader from the bootable disk?
?
MBR (Master Boot Recorder) is located at the first sector of the disk. MBR contains the boot loader.
![](https://i.imgur.com/tSjXqiO.png)


How the bootable device is found in UEFI machines?::

What is the role of the system firmware?::

What is the role of the boot loader?::

What is the most widely used boot loader for linux systems?::GRUB 2 (GRand Unified Bootloader 2)

What is the boot process of RHEL9?
1. When the machine is powered on, system firmware runs the POST 
2. The system firmware looks for the bootable device
3. The system firmware read the boot loader from the bootable device and hand over the control to it.
4. Boot loader displays the boot menu to choose the kernel we would like to boot into.
5. Boot loader loader loads the selected kernel with the initramfs from the boot device to the memory.
6. Boot loader hands over the control to the kernel with parameters.
7. Kernel initialise all the hardware and executes systemd
8. Systemd complete the boot process using the selected boot target and displays the login

How to shut down the system?::`systemctl poweroff` or `shutdown --now`

How to reboot the system?::`systemctl reboot` or `reboot`

