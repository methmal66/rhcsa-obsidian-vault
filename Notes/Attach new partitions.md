---
tags:
  - flashcards
  - rh134/Ch5_Storage
  - todo
  - rh134
  - important
---

In disk partitioning, what are hard drives divided into?::Multiple logical volume storages

# Step1: Create partition table

How to display the available disks?
?
`lsblk`
![450](https://i.imgur.com/8rL7Uby.png)

How to display the partition table of a single disk?
?
`parted /dev/vda print` 
![450](https://i.imgur.com/OFlObAF.png)

How to erase disk and write MBR partition table to it?::`parted /dev/vda mklabel msdos`

How to erase disk and write GPT partition table to it?::`parted /dev/vda mklabel gpt`
# Step2: Create partitions

How to create a new 2GiB primary partition in a MBR disk?::`parted /dev/sda mkpart primary 1M 2001M`

How to create a new extended partition in a MBR disk?::`parted /dev/sda mkpart extended 3G 10.7G`

How to create a new 2GiB partition in a GPT disk?::`parted /dev/sda mkpart partname 1M 2001M`

How to remove a partition from a disk?::`parted /dev/sda rm 2`
# Step3: Create file system

What is the default file system used in RHEL systems?::xfs

What is the default file system in most linux systems?::ext4

What is the legacy file system of old linux systems?::ext3

How to create a xfs file system in a disk?
?
`mkfs.xfs /dev/sda1`
![600](https://i.imgur.com/0I0iIoX.png)

How to create a ext4 file system in a disk?
?
`mkfs.ext4 /dev/sda2`
![600](https://i.imgur.com/qbmb0C1.png)

# Step4: Manually mount partitions

Why partitions are manually mounted?::To verify that a formatted device is accessible and working as expected.

How to manually mount a partition to a mount point?::`mount /dev/sda1 /mnt`

How to manually unmount a partition?::`umount /dev/sda1`

How to view currently mounted file systems, mount points and options of each partition?
?
`mount | gpt /dev/sda1`
![](https://i.imgur.com/5ilgidu.png)

How to view the mount points of all partitions?
?
`lsblk`

# Step5: Permanently mount partitions

Why partitions are permanently mounted?::To configure the system to automatically mount the file system during system boot

How to display the UUID each partition?
?
`lsblk --fs`
![](https://i.imgur.com/5kMAWkn.png)

Which file should be modified to permanently mount partitions?
?
`/etc/fstab`
![700](https://i.imgur.com/AaFMNEJ.png)

How to mount partitions automatically according to the /etc/fstab configs?::`mount -a`

How to make the system daemon loads and uses the new configuration after modifying /etc/fstab?`systemctl daemon-reload`
