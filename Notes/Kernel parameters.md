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
2. Select the kernel entry to boot using arrows and edit it by pressing `e` key.
3. Move the cursor to the end of the line starting with *linux*
4. Add the necessary kernel parameters
5. Press `Ctrl + x` to boot with changes

Which kernel parameter must be added to enter into the initramfs, in order to reset the root password?::`rd.break`

Which kernel parameter must be added to boot the system in rescue mode?::`systemd.unit=rescue.target`

Which kernel parameter must be added to boot the system during an emergency?::`systemd.unit=emergency.target`

