---
tags:
  - flashcards
  - rh134/Ch5_Storage
  - todo
  - rh134
---

![](https://i.imgur.com/FepFlek.png)
Why swap partitions are used?::To supplement the main memory

# Step1: Create swap partitions

How to create a 500MiB swap partition in a MBR disk?
?
`parted /dev/vda mkpart primary linux-swap 3001M 3501M`

How to create a 500MiB swap partition in a GPT disk?
?
`parted /dev/vda mkpart partname linux-swap 3001M 3501M`

# Step2: Format swap space

How to format a partition to be used swap memory?
?
`mkswap /dev/vda1`

# Step3: Manually activate swap

How to activate a swap partition manually?::`swapon /dev/vda1`

How to deactivate a swap partition manually?::`swapoff /dev/vda1`

How to display the swap memory usage?
?
`swapon --show`

or `free`

# Step4: Persistently activate swap

Which file should be modified to permanently mount partitions?
?
`/etc/fstab`
