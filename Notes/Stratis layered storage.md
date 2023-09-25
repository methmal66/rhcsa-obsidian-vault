---
tags:
  - flashcards
  - rh134
  - rh134/Ch5_Storage
---
What is the main benefit of stratis?::Filesystems are automatically expanding (on demand). So no need to create a partitions with specific size at first, then extend it later. 

How to install stratis?
?
`dnf install stratisd stratis-cli`
`systemctl enable --now stratisd`

How to create a stratis pool?:`stratis pool create mypool /dev/vdb`

How to list all the available stratis pools?
?
`stratis pool list`
![](https://i.imgur.com/0RfNS7S.png)

How to list members of a stratis pool?
?
`stratis blockdev list mypool`
![](https://i.imgur.com/GyfqqNR.png)

How to destroy a stratis pool?::`stratis pool destroy mypool`

How to create a filesystem in a stratis pool?::`stratis filesystem create mypool myfs`

How to destroy a stratis filesystem?::`stratis filesystem destroy mypool myfs`

How to take a snapshot of a filesystem?::`stratis filesystem snapshot mypool myfs myfs-snap`

In which filesystem stratis filesystems are created?::xfs

How to permanently mount a stratis filesystem?::Add `UUID=7b57190-8fba-463e-8c8-29c80703d45e /dir1 ×fs defaults,x-systemd.requires=stratisd.service 0 0` to /etc/fstab. There is a special permission

How to expand a pool by adding more disks?::`stratis pool add-data mypool /dev/vdc`

How to list all the available stratis filesystems?
?
![](https://i.imgur.com/xWlZ4eO.png)


