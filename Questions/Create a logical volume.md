---
tags:
  - question
  - rh134/Ch6_LVM
references:
  - "[[Logical Volume Manager]]"
---
Create a volume group, and set the size is 500M, the size of single PE is 16M. Create logical volume named lv0 in this volume group, set size is 20 PE, make it as ext3 file system, and mounted automatically under /mnt/data.

> [!faq]- Answer
> 1. Make a partition 
> `parted /dev/sda mklabel gpt`
> `parted /dev/sda mkpart ext4 0% 500M`
> 2. Create a VG. `vgcreate vg0 -s 16M /dev/sda1`
> 3. Create a LV. `lvcreate vg0 -n lv0 -l 20`
> 4. Format the LV. `mkfs.ext3 /dev/vg0/lv0`
> 5. Mount persistently
> `echo "/dev/vg0/lv0  ext3  defaults  0  0" >> /etc/fstab`
> `mount -a`