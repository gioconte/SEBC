#Checking swappiness
cat /proc/sys/vm/swappiness

60

Temporarily setting it to value of 1.

sudo sysctl vm.swappiness=1

Set vm.swappiness to 1 in a permanet way.

sudo vi /etc/sysctl.conf and add line vm.swappiness=1

Checking volumes

cat /etc/fstab

/etc/fstab
 Created by anaconda on Tue Jul 14 09:33:08 2015

Accessible filesystems, by reference, are maintained under '/dev/disk'
See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info

UUID=0e6b1614-7bbe-4d6e-bc78-a5556a123ba8 /                       ext4    defaults        1 1
tmpfs                   /dev/shm                tmpfs   defaults        0 0
devpts                  /dev/pts                devpts  gid=5,mode=620  0 0
sysfs                   /sys                    sysfs   defaults        0 0
proc                    /proc                   proc    defaults        0 0


Showing that Transparent Huge page is disabled
cat /sys/kernel/mm/redhat_transparent_hugepage/defrag
always madvise [never]








