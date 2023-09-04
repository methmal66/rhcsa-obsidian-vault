#rhcsa #linux #flashcards #rhcsa/rh134/Ch5_Storage 

In disk partitioning, what are hard drives divided into?::Multiple logical volume storages
# Step1: Create partition table
How to display the available disks?
?
`lsblk`

How to display the partition table of a single disk?
?
`parted /dev/vda`

How to erase disk and write MBR partition table to it?`parted /dev/vda mklabel msdos`

How to erase disk and write GPT partition table to it?`parted /dev/vda mklabel gpt`

# Step2: Create partitions
How to create a new 2GiB primary partition in a MBR disk?
?
`parted /dev/vda mkpart primary xfs 1M 2001M`

How to create a new 2GiB partition in a GPT disk?
?
`parted /dev/vda mkpart partname xfs 1M 2001M`

How to remove a partition from a disk?`parted /dev/vda rm 2`

How to create relative device files after creating partitions?::`udevadm settle`
# Step3: Create file system
What is the default file system used in RHEL systems?::xfs

What is the default file system in most linux systems?::ext4

What is the legacy file system of old linux systems?::ext3

How to create a xfs file system in a disk?
?
`mkfs.xfs /dev/vda1`

How to create a ext4 file system in a disk?
?
`mkfs.ext4 /dev/vda1`

# Step4: Manually mount partitions
Why partitions are manually mounted?::To verify that a formatted device is accessible and working as expected.

How to manually mount a partition to a mount point?::`mount /dev/vda1 /mnt`

How to manually unmount a partition?::`mount /dev/vda1`

How to view currently mounted file systems, mount points and options of each partition?
?
`mount | gpt /dev/vda1`

How to view the mount points of all partitions?
?
`lsblk`
# Step5: Permanently mount partitions
Why partitions are permanently mounted?::To configure the system to automatically mount the file system during system boot

How to display the UUID each partition?
?
`lsblk --fs`

Which file should be modified to permanently mount partitions?
?
`/etc/fstab`

How to make the system daemon loads and uses the new configuration after modifying /etc/fstab?`systemctl daemon-reload`

