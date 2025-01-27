# obviously, a single .md cannt describe linux

## Listing block devices
This was on the JR image.
```
ubuntu@ubuntu:~$ sudo lsblk
NAME         MAJ:MIN RM   SIZE RO TYPE MOUNTPOINTS
loop0          7:0    0  94.4M  1 loop /snap/lxd/30134
loop1          7:1    0  68.8M  1 loop /snap/core22/1720
loop2          7:2    0  69.2M  1 loop /snap/core22/1624
loop3          7:3    0  33.7M  1 loop /snap/snapd/21761
loop4          7:4    0  38.7M  1 loop /snap/snapd/23546
loop5          7:5    0 100.1M  1 loop /snap/lxd/31822
mmcblk1      179:0    0  29.5G  0 disk
├─mmcblk1p1  179:1    0     4M  0 part
└─mmcblk1p2  179:2    0  29.5G  0 part /
mmcblk0      179:32   0  58.3G  0 disk
mmcblk0boot0 179:64   0     4M  1 disk
mmcblk0boot1 179:96   0     4M  1 disk
nvme0n1      259:0    0 465.8G  0 disk
```

> what are loopx?

### SDCard
This is mmcblk1 which is 32 GB.
It was flashed with BalenaEtcher.
It has two partitions, the small one is probably the bootloader.
The larger is the root file system.

### eMMC
This is evidently mmblk0, 64 GB.
There are two additional block device which seem to be related.

### NVME SSD
This is clearly nvme0n1, which is 500 GB

### loopn and snap
These are some kind of snap hot storage.
Maybe they are the result of installed apt packages, 6 seems about right.

``snap remove <package-name>`

> LXD - container and VM manager
