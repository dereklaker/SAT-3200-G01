
# Lab 3
#TODO: Screenshots
## Creation of Storage Pools
We started at Pool ID 10
| ID | Level | Title | Size | Mountpoint |
|---|---|---|---|---|
|test|test2|test3|test4|test5|


|10|RAID5|group1-homes|300GB|/storage/home|
|11|RAID10|group1-database|300GB|/storage/database|
|12|RAID10|group1-finance-hr|200GB|/storage/finance-hr|
|13|RAID10|group1-logs|100GB|/storage/logs|
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
