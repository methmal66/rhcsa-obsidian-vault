---
tags:
  - flashcards
  - rh134/Ch5_Storage
  - todo
  - rh134
  - important
---

![](https://i.imgur.com/FepFlek.png)

Why swap partitions are used?::To supplement the main memory

# Step1: Create swap partitions
How to create a 500MiB swap partition in a MBR disk?::`parted /dev/vda mkpart primary linux-swap 3001M 3501M`

How to create a 500MiB swap partition in a GPT disk?::`parted /dev/vda mkpart partname linux-swap 3001M 3501M`
# Step2: Format swap space
How to format a partition to be used swap memory?
?
`mkswap /dev/sdb1`
![500](https://i.imgur.com/7z6ObZZ.png)
# Step3: Manually activate swap
How to activate a swap partition manually?::`swapon /dev/sdb2`

How to deactivate a swap partition manually?::`swapoff /dev/sdb2`

How to display the swap memory usage?
?
`swapon --show`
![300](https://i.imgur.com/OabUbPH.png)
# Step4: Persistently activate swap

Which file should be modified to permanently mount partitions?
?
`/etc/fstab`
![600](https://i.imgur.com/57G2ruB.png)
