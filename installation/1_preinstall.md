#Checking swappiness
cat /proc/sys/vm/swappiness

60

Temporarily setting it to value of 1.

sudo sysctl vm.swappiness=1

Set vm.swappiness to 1 in a permanet way.

sudo vi /etc/sysctl.conf and add line vm.swappiness=1

#Checking volumes

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


[ec2-user@ip-172-31-21-145 ~]$ df -hP

Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1      9.8G  1.7G  7.6G  19% /
tmpfs           7.3G     0  7.3G   0% /dev/shm


#Showing that Transparent Huge page is disabled

cat /sys/kernel/mm/redhat_transparent_hugepage/defrag

always madvise [never]

#Checking Network interfaces

[ec2-user@ip-172-31-21-145 ~]$ netstat -i

Kernel Interface table
Iface       MTU Met    RX-OK RX-ERR RX-DRP RX-OVR    TX-OK TX-ERR TX-DRP TX-OVR Flg
eth0       9001   0     1608      0      0      0     1366      0      0      0 BMRU
lo        65536   0        0      0      0      0        0      0      0      0 LRU

nslookup ip-172-31-21-145.eu-central-1.compute.internal
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
Name:	ip-172-31-21-145.eu-central-1.compute.internal
Address: 172.31.21.145

[ec2-user@ip-172-31-21-145 ~]$ nslookup ip-172-31-21-141.eu-central-1.compute.internal
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
Name:	ip-172-31-21-141.eu-central-1.compute.internal
Address: 172.31.21.141

[ec2-user@ip-172-31-21-145 ~]$ nslookup ip-172-31-21-142.eu-central-1.compute.internal
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
Name:	ip-172-31-21-142.eu-central-1.compute.internal
Address: 172.31.21.142

[ec2-user@ip-172-31-21-145 ~]$ nslookup ip-172-31-21-143.eu-central-1.compute.internal
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
Name:	ip-172-31-21-143.eu-central-1.compute.internal
Address: 172.31.21.143

[ec2-user@ip-172-31-21-145 ~]$ nslookup ip-172-31-21-144.eu-central-1.compute.internal
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
Name:	ip-172-31-21-144.eu-central-1.compute.internal
Address: 172.31.21.144











