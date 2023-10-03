---
tags:
  - question
  - important
---
Do the following configurations in the given virtual machine
>[!note] Initial setup
>1. Create the partition table. `parted /dev/vdb mklabel gpt` 
>2. Create a single partition`parted /dev/vdb mkpart first %0 1000MB`
>3. Create a PV `pvcreate /dev/vdb1`
>4. Create a VG `vgcreate mygrp /dev/vdb1`
>5. Create a LV `lvcreate mygrp -n myvol1 -L 190M`
>6. Format the filesystem `mkfs.ext4 /dev/vdb1`

1. Change the logical volume capacity named myvol1 from 190M to 250M
>[!faq]- Answer
>1. Extend LV with filesystem extend `lvextend mygrp/myvol1 -r -L 250M`
>2. Verify `lvs`

2. Create a volume group named wgroup, and set extend size as 8MiB. And create a logical volume containing 100 extends and set name wshare, format with xfs filesystem, and mount automatically under /mnt/wshare