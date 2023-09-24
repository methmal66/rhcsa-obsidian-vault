---
tags:
  - interview
  - important
references:
  - https://youtu.be/b-m0Oz_8W3k?si=KX3301uWWHADwh7M&t=225
  - https://www.redhat.com/sysadmin/configure-nfs-linux
---
# Set up server
1. Enable **nfs-utils** and **rpcbind** services
`dnf install -y nfs-utils`
`systemctl enable --now nfs-utils`
`systemctl enable --now rpcbind`

2. Set permissions
`chown root:staff /nfs`
`chmod 2770 -R /nfs`

3. Export the shared directory
`echo "/nfs 192.168.10.0/24(rw)" >> /etc/exports`
`exportfs -r`

4. Allow from firewall
`firewall-cmd --add-service nfs --permanent`
Port no is **2049**

# Set up client
Mount the nfs
`echo "192.168.10.100:/nfs  /nfs  nfs  rw  0   0" >> /etc/fstab`
`mount -a`