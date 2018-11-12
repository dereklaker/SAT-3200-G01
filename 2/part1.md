# Lab 2
## Installing HostAgent
    Plug in the flash drive with the .rpm files stored on it
    Mount the flash drive
```
mount /dev/sdX /mnt
cd /mnt/SANS
yum localinstall -y ./repo/*
```
## Troubleshooting
    Dependecy resolution initally failed
    Plugged into the NAT switch
    Set gateway to 172.20.189.1
    DNS: 8.8.8.8
```
yum update -y
```
    Repeat "Installing HostAgent"
## Agent Config
    /etc/Unisphere/agent.config
```
clarDescr Navisphere Agent
clarContact Group1, EERC 328
device auto auto

user group1uni@172.20.189.113
user system@172.20.189.113

poll 60
eventlog 100
baud 9600
```
## Agent ID Config
    /root/agentID.txt
```
sat3200-g01
172.20.189.113
```
## Hosts Config
    /etc/hosts
```
172.20.189.113  sat3200-g01
```
## Restarting hostagent
```
service hostagent restart
```
## WWNS
```
cat /sys/class/fc_host/host[2-3]/port_name

>>>
0x2100001b328edb93
9x2101001b32aedb93
```

## Create Initiator Record
![](https://cdn.discordapp.com/attachments/143171303296204801/511345459139444757/1.png)
