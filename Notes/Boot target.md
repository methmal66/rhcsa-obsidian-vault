---
tags:
  - rh134
  - rh134/Ch8_Boot
  - flashcards
required:
  - "[[Controlling services]]"
aliases:
  - Systemd target
---
What is a systemd target?::A set of systemd units that the system should start to reach a desired state

Which boot target provides a text based only logins for multiple users?::multi-user.target

Which boot target provides a both graphical and text-based logins for multiple users?::graphical.target

Which boot target is used for a rescue when the system fails to boot?::rescue.target

Which boot target provides read only permissions during an emergency?::emergency.target

How to list all the available targets?
?
`systemctl  list-units --type=target --all`

How to list the dependencies of a target?
?
`systemctl list-dependencies graphical.target`

How to switch to a different target by immediately rebooting the system?::`systemctl isolate multi-user.target`

Where is the default target is configured?::In /etc/systemd/system/default.target as a symbolic link (Dont manually edit this)

How to find the default target?::`systemctl get-default`

How to set the default target, so the system will boot into it from the next boot onwards?::`systemctl set-default graphical.target`

Which kernel parameter must be given to select a different target at boot time?::`systemd.unit=graphical.target`

