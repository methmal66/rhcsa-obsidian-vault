---
tags:
  - flashcards
  - rh134/Ch4_SELinux
  - rh134
  - important
---

What does SELinux means?::Security Enhanced Linux

What problem cannot be solved from file permissions?::Files being used for unintended purposes. How files are used

What does SELinux consist of?::Application specific policies defined by developers

Which SELinux mode enforces the loaded policies?::Enforcing

What is the default SELinux mode?::Enforcing

What happens under enforcing mode, when no entry is created for a specific process-resource-action relationship?::That action is denied

What happens when an action is denied?::The attempt is logged with other useful info

What do most access denials indicate?::SELinux is working properly by blocking improper actions.

Which SELinux mode loads the policies and is active, but instead of enforcing access control rules, it logs access violations?::Permissive

Which SELinux mode is helpful for testing and troubleshooting applications and rules?::Permissive

In which mode, SELinux is turned off?::Disabled

In which mode SELinux violations are neither denied nor logged?::Disabled

How to properly disable SELinux?::By using kernel parameters at the boot time

What is the primary goal ofSELinux?::To protect user data from improper use by compromised applications or system services.

How to find the current SELinux mode?
?
`getenforce`

How to set the SELinux mode to enforcing?
?
`setenforce 1`

How to set the SELinux mode to permissive?
?
`setenforce 0`

What is the kernel parameter requires to boot the system into permissive mode?::`enforcing=0`

What is the kernel parameter requires to boot the system into enforcing mode?::`enforcing=1`

What is the kernel parameter requires to enable SELinux at the boot time?::`selinux=1`

What is the kernel parameter requires to disable SELinux at the boot time?::`selinux=0`

Why it is recommended to reboot the system when the SELinux mode is switched from permissive to enforcing?::To ensures that the services started in permissive mode are confined in the next boot.

What is the default config file of SELinux?::/etc/selinux/config

How to set the default SELinux mode?::By editing the /etc/selinux/config file

What happens when both kernel parameters and default configurations exist?::Kernel parameters override the configuration file
