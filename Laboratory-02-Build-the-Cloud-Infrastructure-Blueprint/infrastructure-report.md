# Cloud Infrastructure Assessment Report

## Operating System
- **Operating System:** Ubuntu 24.04

## Kernel Version
- **Kernel Version:** 6.8.0-13-generic

## CPU Information
- **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
- **Number of CPU Cores:** 1

## Memory
- **Total RAM:** 1.9 GiB

## Disk
- **Disk Capacity:** 19G
- **Used Space:** 5.4G
- **Available Space:** 13G

## Mounted File Systems
```
Filesystem      Size  Used Avail Use% Mounted on
tmpfs           191M 1020K  190M   1% /run
/dev/vda1        19G  5.4G   13G  30% /
tmpfs           5.4M     0   5.4M   0% /run/lock
/dev/vda16      881M  117M  703M  15% /boot
/dev/vda15      105M  6.2M   99M   1% /boot/efi
tmpfs           191M  8.0K  191M   1% /run/user/1001
```

## Hostname
- **Hostname:** ubuntu

## IP Address
- **IP Address(es):** 172.30.1.2 (enp1s0), 172.17.0.1 (docker0)

## Linux Commands Used
```bash
cat /etc/os-release
uname -r
lscpu
nproc
free -h
df -h
findmnt
hostname
hostname -I
ip -br addr
```
