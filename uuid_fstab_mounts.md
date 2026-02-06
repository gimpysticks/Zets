---
created: 2026-01-06
---
NAME SIZE TYPE MOUNTPOINT UUID
loop0 104.2M loop /snap/core/17247  
loop1 50.9M loop /snap/snapd/25577  
loop2 239M loop /snap/wps-office/1  
loop3 50.8M loop /snap/snapd/25202  
loop4 105M loop /snap/core/17272  
sda 111.8G disk /media/sticks/PNY FDDD-E3D2
sdb 0B disk  
sdc 465.8G disk  
└─sdc1 465.8G part 52efaa72-2246-482a-8100-26d00308abc3
sdd 1.8T disk  
├─sdd1 1022M part /boot/efi 0536-FC2D
├─sdd2 4G part /recovery 0536-FC3C
├─sdd3 1.8T part / 85527f95-f72d-4b17-a24d-ae9eb72212c1
└─sdd4 4G part c83c29e7-98d7-4852-9759-b6af62252918
└─cryptswap 4G crypt [SWAP] 72672edf-b2fd-4b89-84af-0340706f1136
sde 3.6T disk  
├─sde1 128M part  
└─sde2 3.6T part /media/sticks/ADATA HD710 PRO 86AE88B4AE889E75
zram0 16G disk [SWAP]  
nvme0n1 465.8G disk  
├─nvme0n1p1 1022M part 1B4A-FD8D
├─nvme0n1p2 4G part 1B4A-FD37
├─nvme0n1p3 456.8G part 0fa6644d-ce02-430a-98b0-6884238b4137
└─nvme0n1p4 4G part da5a607c-10d4-4be6-ab4e-1efe3977eab8

# /etc/fstab: static file system information.

#

# Use 'blkid' to print the universally unique identifier for a

# device; this may be used with UUID= as a more robust way to name devices

# that works even if disks are added and removed. See fstab(5).

#

# <file system> <mount point> <type> <options> <dump> <pass>

PARTUUID=9e3a39d9-51e0-4a17-a81b-d7a314268425 /boot/efi vfat umask=0077 0 0
PARTUUID=f6af3832-694a-45a9-9b81-d95ccba973df /recovery vfat umask=0077 0 0
UUID=85527f95-f72d-4b17-a24d-ae9eb72212c1 / ext4 noatime,errors=remount-ro 0 1
/dev/mapper/cryptswap none swap defaults 0 0
192.168.4.2:/data/backup /mnt/backup nfs vers=3,proto=tcp,defaults 0 0
192.168.4.2:/data/Movies /mnt/movies nfs vers=3,proto=tcp,defaults 0 0
192.168.4.2:/data/Pictures /mnt/pictures nfs vers=3,proto=tcp,defaults 0 0
192.168.4.2:/data/Videos /mnt/videos nfs vers=3,proto=tcp,defaults 0 0
192.168.4.2:/data/Documents /mnt/Documents nfs vers=3,proto=tcp,defaults 0 0
192.168.4.2:/data/Music /mnt/music nfs vers=3,proto=tcp,defaults 0 0
192.168.4.2:/data/disk_images /mnt/diskImages nfs vers=3,proto=tcp,defaults 0 0
