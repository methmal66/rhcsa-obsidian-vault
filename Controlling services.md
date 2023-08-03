#linux #flashcards #rhcsa #rhcsa/rh124/Ch9_Services

What is a daemon?::A process running in the background

What is the program that manages daemons in linux?::`systemd`

What is the first process (process with PID = 1) that start in a linux system?::systemd

What is the main systemd unit type?::service

Which type of systemd units are used for system services and frequently access daemons?::.service

Which type of systemd units are used for inter process communication sockets, which should be monitored by systemd?::.socket

Which type of sytemd units are used to delay the activation of a service, until a specific file system change occurs?::.path

How to list all units with their corresponding state?::`sytemctl`

How to list all the service units in the system with their corresponding state?::`systemctl list-units --type service`

How to view the status of a service?::`systemctl status sshd`

How to find if a service is active?::`systemctl is-active sshd`

How to find if a service is enabled?::`systemctl is-enabled sshd`

How to start a service?::`systemctl start sshd`

How to stop a service?::`systemctl stop sshd`

How to restart a service?::`systemctl restart sshd`

How to reload a service?::`systemctl reload sshd`

How to enable a service?::`systemctl enable sshd`

How to disable a service?::`systemctl disable sshd`

How to mask a service?
?
`systemctl mask nftables` or 
`ln -s /dev/null /etc/systemd/system/nftables.service`

How to start and enable a service at the same time?::`systemctl enable --now sshd`

How to stop and disable a service at the same time?::`systemctl disable --now sshd`

What happens in a service restart?::It start the service with a new PID immediately after stoping it

What happens in a service reload?::It reloads only the resources while keeping the PID same

What happens in a service enable?::It configure the service to start automatically on reboots

What happens in a service disable?::It configure the service not to start automatically on reboots.

What happens when a service is masked?::It is impossible to load the service, even if another enabled service requires it

Why it is not recommended to unmask a service?::Because they have masked the service to prevent it from running

What is means as a service is in the static state?::That service is controlled by kernel, users has no control over it

Why it is not recommended to restart a service on a production server?::Because there will be a downtime

What is the purpose of the cgroup (control group)?:: Allocate resources such as CPU time, system memory, network bandwidth to a service

References:
- [Chapter9, Section1, Identifying automatically started system processes](rh124-8.0-student-guide.pdf#pageno=pageno=294)
- [Chapter, Section2, Controlling system services](rh124-8.0-student-guide.pdf#pageno=303)
Related:
- [[Monitoring Processes]]
- [[Signalling processes]]
