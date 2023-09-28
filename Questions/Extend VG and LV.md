---
tags:
  - question
  - rh134/Ch5_Storage
references:
  - "[[Logical Volume Manager]]"
---
We are working on /data initially the size is 2GB. The /dev/test0/lvtestvolume is mount on /data. Now you required more space on /data but you already added all physical volumes belongs to the disk. You saw that you have unallocated space around 5 GB on your hard disk. Increase the size of lvtestvolume by 5GB.

> [!faq]- Answer
> 1. Create a partition from the unallocated space `parted /dev/sda1 mkpart ext4 15GB 100%`
> 2. Create a PV from that partition `pvcreate /dev/sda2`
> 3. Extend our VG with that PV `vgextend test0 /dev/sda2`
> 4. Extend our LV with filesystem resizing `lvextend test0/lvtestvolume -r -L +5GB`