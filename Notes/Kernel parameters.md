---
tags:
  - rh134
  - rh134/Ch8_Boot
  - flashcards
  - important
---
What are the steps to provide kernel parameters on boot time?
?
1. Reboot the system and interrupt the boot loader countdown by pressing any key (other than the enter)
![600](https://i.imgur.com/ZtRWccE.png)

2. Select the kernel entry to boot using arrows and edit it by pressing `e` key.
![600](https://i.imgur.com/AB7a1Yu.png)

4. Move the cursor to the end of the line starting with *linux*
5. Add the necessary kernel parameters
6. Press `Ctrl + x` to boot with changes

Which kernel parameter must be added to enter into the initramfs, in order to reset the root password?::`rd.break`

Which kernel parameter must be added to boot the system in rescue mode?::`systemd.unit=rescue.target`

Which kernel parameter must be added to boot the system during an emergency?::`systemd.unit=emergency.target`

