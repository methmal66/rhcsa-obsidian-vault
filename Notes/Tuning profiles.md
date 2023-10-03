---
tags:
  - rh134
  - rh134/Ch3_Tuning
  - review
aliases:
  - Tuned daemon
---
> [!faq] How to enable tuned daemon?
> 1. `dnf install tuned`
> 2. `systemctl enable --now tuned`

>[!faq] What is the main config file of tuned?
/etc/tuned/tuned-main.conf

 >[!faq] How to enabled dynamic tuning?
 >1. Edit `/etc/tuned/tuned-main.conf` file and set the *dynamic_tuning* variable to *1*
 >2. `systemctl restart tuned`

>[!faq] How to find the currently active tuning profile?
`tuned-adm active`

>[!faq] How to find the recommended tuning profile for our system?
>`tuned-adm recommend`

>[!faq] How to switch to a different active profile?
>`tuned-adm profile througput-performance`

Why tuned daemon is being used?
	Tuned daemon applies tuning adjustments to optimise the system performance for selected profiles

How static tuning is applied?
	Tuned daemon applies kernel parameters at the boot time, so the system runs in according to the pre defined profile.

How dynamic tuning is applied?
	Tuned daemon continuously monitors system activity and adjusts settings according to runtime behaviour changes.

What are the monitor plug-ins used by tuned to analyse the system and obtain information from it?
	- Disk (Monitor I/O operations of each disk)
	- Net (Monitor transferred packets in each NIC)
	- Load (Monitor the load of every CPU)

What are the tuning plugs-ins used by tuned?
	- Disk (Configure Disk scheduler, spin-down timeout, advanced power management, ...)
	- Net (Configure interface speed, Wake-On-LAN, ...)
	- CPU (Configure governor, latency, ...)
 
What are the two categories of tuned profiles?
	1. Power-saving profiles
	2. Performance-boosting profiles

What are the aspects performance-boosting profiles focus on?
	- Low latency for storage and network
	- High throughout for storage and network
	- Virtual machine performance
	- Virtualisation host performance

How to see the configs of a profile?
	`cat /usr/lib/tuned/virtual-guest/tuned.conf`

How to list all the available tuning profiles?
	`tuned-adm list`


