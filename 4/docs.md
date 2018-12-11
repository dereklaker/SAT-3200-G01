# Lab 4

## Storage mount points
`/storage/raid10tset`
`/storage/raid3test`

## Commands to configure LUNS
`/root/scripts/ql-scan-luns.sh -s`
`powermt display dev=all`

## Create a partition
`sudo parted -a optimal /dev/sda mklabel gpt mkpart primary 0% 100%`
Or use `fdisk`

## Create a filesystem
`mkfs -t ext4 /dev/emcpower(f,g)`

## Mount your filesystem
`mount /dev/emcpower(f,g) /path/to/locaion`

## Modify Power Path policy for LUNs
`powermt set policy=re dev=emcpower(f) -> Request`
`powermt set policy=re dev=emcpower(b) -> Request`
`powermt set policy=li dev=emcpower(g) -> Least I/O`

## Modify Power Path priority or LUNs -- SKIPPED
`powermt set priority=10 dev=emcpower(b)`

## Set paths to standby on both LUNs
`powermt set mod=standby hba=4 dev=emcpower(b,)`

## bonnie++ testing
`bonnie++ -d /path/to/test -u USERNAME > /path/to/log/out.log`
`bonnie++ -d /path/to/directory -u USERNAME > $(date +%Y%m%d-%H%M%S).log`

## Performance testing
- Storage
- Luns
- Right click on your LUN to analyze
- Select analyzer
- Performance analyzer
