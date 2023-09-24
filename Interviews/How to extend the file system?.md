---
tags:
  - interview
  - important
references:
  - https://youtu.be/b-m0Oz_8W3k?si=lTCe1ud2_4wuczs6&t=930
---
In LVM, only one volume group is created using all the available storage. So, we dont have to extend the volume group.

1. Extend the volume group
`lvextend vg01/lv01 -L +10G`

2. Grow the filesystem
For ext4, `resize2fs /dev/vg01/lv01`
For xfs, `grow_fs /dev/vg01/lv01`

3. Verify the config
`lvs`