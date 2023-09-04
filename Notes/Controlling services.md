#linux #flashcards #rhcsa #rhcsa/rh124/Ch9_Services

What is a daemon?::A process running in the background
<!--SR:!2023-08-08,4,270-->

What is the program that manages daemons in linux?::`systemd`
<!--SR:!2023-08-08,4,270-->

What is the first process (process with PID = 1) that start in a linux system?::systemd
<!--SR:!2023-08-07,3,250-->

What is the main systemd unit type?::service
<!--SR:!2023-08-08,4,270-->

Which type of systemd units are used for system services and frequently access daemons?::.service
<!--SR:!2023-08-08,4,270-->

Which type of systemd units are used for inter process communication sockets, which should be monitored by systemd?::.socket
<!--SR:!2023-08-08,4,270-->

Which type of sytemd units are used to delay the activation of a service, until a specific file system change occurs?::.path
<!--SR:!2023-08-05,1,230-->

How to list all units with their corresponding state?::`sytemctl`
<!--SR:!2023-08-07,3,250-->

How to list all the service units in the system with their corresponding state?::`systemctl list-units --type service`
<!--SR:!2023-08-08,4,270-->

How to view the status of a service?::`systemctl status sshd`
<!--SR:!2023-08-08,4,270-->

How to find if a service is active?::`systemctl is-active sshd`
<!--SR:!2023-08-08,4,270-->

How to find if a service is enabled?::`systemctl is-enabled sshd`
<!--SR:!2023-08-08,4,270-->

How to start a service?::`systemctl start sshd`
<!--SR:!2023-08-08,4,270-->

How to stop a service?::`systemctl stop sshd`
<!--SR:!2023-08-08,4,270-->

How to restart a service?::`systemctl restart sshd`
<!--SR:!2023-08-08,4,270-->

How to reload a service?::`systemctl reload sshd`
<!--SR:!2023-08-08,4,270-->

How to enable a service?::`systemctl enable sshd`
<!--SR:!2023-08-08,4,270-->

How to disable a service?::`systemctl disable sshd`
<!--SR:!2023-08-08,4,270-->

How to mask a service?
?
`systemctl mask nftables` or 
`ln -s /dev/null /etc/systemd/system/nftables.service`
<!--SR:!2023-08-08,4,270-->

How to start and enable a service at the same time?::`systemctl enable --now sshd`
<!--SR:!2023-08-08,4,270-->

How to stop and disable a service at the same time?::`systemctl disable --now sshd`
<!--SR:!2023-08-08,4,270-->

What happens in a service restart?::It start the service with a new PID immediately after stoping it
<!--SR:!2023-08-08,4,270-->

What happens in a service reload?::It reloads only the resources while keeping the PID same
<!--SR:!2023-08-08,4,270-->

What happens in a service enable?::It configure the service to start automatically on reboots
<!--SR:!2023-08-08,4,270-->

What happens in a service disable?::It configure the service not to start automatically on reboots.
<!--SR:!2023-08-08,4,270-->

What happens when a service is masked?::It is impossible to load the service, even if another enabled service requires it
<!--SR:!2023-08-07,3,250-->

Why it is not recommended to unmask a service?::Because they have masked the service to prevent it from running
<!--SR:!2023-08-08,4,270-->

What is means as a service is in the static state?::That service is controlled by kernel, users has no control over it
<!--SR:!2023-08-08,4,270-->

Why it is not recommended to restart a service on a production server?::Because there will be a downtime
<!--SR:!2023-08-08,4,270-->

What is the purpose of the cgroup (control group)?:: Allocate resources such as CPU time, system memory, network bandwidth to a service
<!--SR:!2023-08-08,4,270-->

References:
- [Chapter9, Section1, Identifying automatically started system processes](rh124-rhel8-official-student-workbook.pdf#pageno=pageno=294)
- [Chapter, Section2, Controlling system services](rh124-rhel8-official-student-workbook.pdf#pageno=303)
Related:
- [[Monitoring Processes]]
- [[Signalling processes]]
