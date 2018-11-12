
# Lab 3
#TODO: Screenshots
## Creation of Storage Pools
We started at Pool ID 10
Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
## Adding Pools to groups
Go to each LUN and add the storage group
## Rescan RHEL devices
```
./scripts/ql-scan-lun.sh
```
## Add License Key
```
emcpreg -add key KEY
```
## Creating partitions
```
parted -a optimal /dev/sdX mklabel gpt mkpart primary 0% 100%
```
## Creating file systems
```
mkfs -t ext4 /dev/empcpowerN1
```
## Mounting file systems
```
mount -t ext4 /dev/emcpowerN1 /path/to/mount
```
## Creating users
```
useradd -m -s /bin/zsh -d /path/to/home/username username
```
## Setting passwords
```
sudo passwd username
```
