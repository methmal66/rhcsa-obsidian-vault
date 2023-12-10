---
tags:
  - flashcards
  - rh134
  - rh134/Ch6_LVM
  - important
required:
  - "[[Attach new partitions]]"
---
Why LVM is used?::To overcome the limitation of physical partitions

What is the main benefit of LVM?::Partitions can be resized easily

What are used by logical volumes to store data?::Physical volumes

What can be used to create a PV?::An entire disk or a partition of it

What are the steps of creating logical volumes?
?
1. Convert physical disks to physical volumes (PVs)
2. Create an one large volume group (VG) by combining all those PVs
3. Divid the VG into smaller logical volumes(LVs) as how you would partition a physical disk

How to create PVs?::`pvcreate /dev/sda /dev/sdb2`

How to display all the available PVs?
?
`pvs`
![](https://i.imgur.com/vGfEhSg.png)

How to remove a PV?::`pvremove /dev/sda`

How to display info of a single PV?
?
`pvdisplay /dev/sdb`
![](https://i.imgur.com/jdJIWQe.png)

How to create a VG?::`vgcreate vg01 /dev/sda /dev/sdb2`

How to display all the available VGs?::`vgs`
![](https://i.imgur.com/ZpwumVV.png)

How to remove a VG?::`vgremove /dev/vg01`

How to display info of about a single VG?
?
`vgdisplay vg01` or `vgdisplay /dev/vg01`
![](https://i.imgur.com/yAjtRae.png)

How to create a LV?::`lvcreate vg01 -n lv01 -L 10G`

How to display all the available LVs?::`lvs`
![](https://i.imgur.com/IwtGBVV.png)

How to display info about a single LV?
?
`lvdisplay vg01/lv01` or `lvdisplay /dev/vg01/lv01`
![](https://i.imgur.com/335ECd7.png)

How to remove a LV?::`lvremove /dev/vg01/lv01`

How to extend a LV, if there is enough space in that VG?::`lvextend vg01/lv01 -L +5G` or `/lvextend vgo1/lv01 -L +500M`

How to extend a VG, if there is no additional space?::`vgextend vg01 /dev/vdc`

How to grow an ext4 filesystem when a LV is extended?::`resize2fs /mnt/data`

How to grow a xfs filesystem when a LV is extended?::`xfs_growfs /mnt/data`

How to format a swap LV after extending?::As how you would normally do it, `mkswap /dev/vg01/swap`

