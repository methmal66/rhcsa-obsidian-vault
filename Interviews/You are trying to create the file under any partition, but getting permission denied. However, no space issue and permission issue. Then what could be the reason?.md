---
tags:
  - interview
  - important
references:
  - https://youtu.be/cFhWlBkeGxA?si=oGnuPOjfhvSLCHfn&t=659
related:
  - "[[inode depletion]]"
---
Running out of inodes. Delete or archive unwanted files to reuse inodes

- Check the fs space using `df -h /mnt`
- Check the inode usage `df -i /mnt`
