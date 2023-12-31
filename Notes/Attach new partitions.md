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

>[!faq] How to display the available disks?::`lsblk`

>[!faq]  How to display the partition table of a single disk?::`parted /dev/vda print` 

>[!faq] How to erase disk and write MBR partition table to it?::`parted /dev/vda mklabel msdos`

>[!faq] How to erase disk and write GPT partition table to it?::`parted /dev/vda mklabel gpt`
# Step2: Create partitions

>[!faq] How to create a new 2GiB primary partition in a MBR disk?::`parted /dev/sda mkpart primary 1M 2001M`

>[!faq] How to create a new extended partition in a MBR disk?::`parted /dev/sda mkpart extended 3G 10.7G`

>[!faq] How to create a new 2GiB partition in a GPT disk?::`parted /dev/sda mkpart partname 1M 2001M`

>[!faq] How to remove a partition from a disk?::`parted /dev/sda rm 2`
# Step3: Format partitions

>[!faq] How to format a partition into xfs filesystem?::`mkfs.xfs /dev/sda1`

>[!faq] How to format a partition into ext4 filesystem?::`mkfs.ext4 /dev/sda1`


What is the default file system used in RHEL systems?
	xfs

What is the default file system in most linux systems?
	ext4

What is the legacy file system of old linux systems?
	ext3
# Step4: Manually mount partitions

>[!faq] How to manually mount a partition to a mount point?::`mount /dev/sda1 /mnt`

>[!faq] How to manually unmount a partition?::`umount /dev/sda1`

>[!faq] How to view the mount points of all partitions?::`lsblk`

Why partitions are manually mounted?
	To verify that a formatted device is accessible and working as expected.

How to view currently mounted file systems, mount points and options of each partition?
	`mount | gpt /dev/sda1`![](https://i.imgur.com/5ilgidu.png)
# Step5: Automatically mount partitions

>[!faq] How to display the UUID each partition?::`lsblk --fs`

>[!faq] Which file should be modified to permanently mount partitions?::`/etc/fstab`

>[!faq] How to mount partitions automatically according to the /etc/fstab configs?::`mount -a`

Why partitions are permanently mounted?
	To configure the system to automatically mount the file system during system boot
