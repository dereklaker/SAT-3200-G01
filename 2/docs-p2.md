# Lab 2 p 2
## Create a group storage name
Hosts->Storage Groups->Create Group->Properties
Name: sat3200-g01-storage
![](https://cdn.discordapp.com/attachments/143171303296204801/511348187290927104/1.png)
## Add the host
Move your host to the right side
![](https://cdn.discordapp.com/attachments/143171303296204801/511348535543726101/1.png)
## Create a new RAID Group
Storage->Storage Configuration->Storage Pools->Create RAID Group
![](https://cdn.discordapp.com/attachments/143171303296204801/511350771955138570/1.png)
## Our First Lun
We called this sat3200-g01-first-LUN
![](https://cdn.discordapp.com/attachments/143171303296204801/511351404758302720/1.png)
## Add the LUN to our group
Hosts->Storage
![](https://cdn.discordapp.com/attachments/143171303296204801/511353368472584203/1.png)
## Verified the host applied to the storage
This should have your IP in it
![](https://media.discordapp.net/attachments/489942840827183125/511642442274045962/unknown.png)
## Zoning
This is also detailed in the lab 2 discussion
![](https://media.discordapp.net/attachments/489942840827183125/511642910459166731/unknown.png)
Make sure you commit with:
```
zone commit vsan 1
```
## Refreshing the LUN Groups:
Refresh the existing LUN initiator by going to Storage->Initiators then,
- Click the existing LUN Group
- Remove your host
- Apply
- Re add your host
- Apply

Refresh the SCSI Bus and Rescan
```
./scripts/ql-scan-lun
```

## Viewing LUN Groups
```
powermt display dev=emcpowerX
```
