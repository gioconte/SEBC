#Checking swappiness
```
cat /proc/sys/vm/swappiness
60
```
Temporarily setting it to value of 1.
```
sudo sysctl vm.swappiness=1
```
Set vm.swappiness to 1 in a permanet way.
```
sudo vi /etc/sysctl.conf and add line vm.swappiness=1
```
#Checking volumes
```
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


[ec2-user@ip-172-31-21-145 ~]$ df -h

Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1      9.8G  1.7G  7.6G  19% /
tmpfs           7.3G     0  7.3G   0% /dev/shm
```

#Showing that Transparent Huge page is disabled
```
cat /sys/kernel/mm/redhat_transparent_hugepage/defrag

always madvise [never]
```
#Checking Network interfaces
```
[ec2-user@ip-172-31-21-145 ~]$ netstat -i

Kernel Interface table
Iface       MTU Met    RX-OK RX-ERR RX-DRP RX-OVR    TX-OK TX-ERR TX-DRP TX-OVR Flg
eth0       9001   0     1608      0      0      0     1366      0      0      0 BMRU
lo        65536   0        0      0      0      0        0      0      0      0 LRU


[ec2-user@ip-172-31-21-145 ~]$ ifconfig 
eth0      Link encap:Ethernet  HWaddr 06:84:28:5F:68:05  
          inet addr:172.31.21.145  Bcast:172.31.31.255  Mask:255.255.240.0
          inet6 addr: fe80::484:28ff:fe5f:6805/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:55451 errors:0 dropped:0 overruns:0 frame:0
          TX packets:11353 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000 
          RX bytes:77932950 (74.3 MiB)  TX bytes:997117 (973.7 KiB)
          Interrupt:145 

lo        Link encap:Local Loopback  
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0 
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)
```

##Getent forward and reverse lookups
```
[ec2-user@ip-172-31-21-145 ~]$ getent ahosts ip-172-31-21-145.eu-central-1.compute.internal
172.31.21.145   STREAM ip-172-31-21-145.eu-central-1.compute.internal
172.31.21.145   DGRAM  
172.31.21.145   RAW  

[ec2-user@ip-172-31-21-145 ~]$ getent ahosts ip-172-31-21-141.eu-central-1.compute.internal
172.31.21.141   STREAM ip-172-31-21-141.eu-central-1.compute.internal
172.31.21.141   DGRAM  
172.31.21.141   RAW    

[ec2-user@ip-172-31-21-145 ~]$ getent ahosts ip-172-31-21-142.eu-central-1.compute.internal
172.31.21.142   STREAM ip-172-31-21-142.eu-central-1.compute.internal
172.31.21.142   DGRAM  
172.31.21.142   RAW    

[ec2-user@ip-172-31-21-145 ~]$ getent ahosts ip-172-31-21-143.eu-central-1.compute.internal
172.31.21.143   STREAM ip-172-31-21-143.eu-central-1.compute.internal
172.31.21.143   DGRAM  
172.31.21.143   RAW   

[ec2-user@ip-172-31-21-145 ~]$ getent ahosts ip-172-31-21-144.eu-central-1.compute.internal
172.31.21.144   STREAM ip-172-31-21-144.eu-central-1.compute.internal
172.31.21.144   DGRAM  
172.31.21.144   RAW  

[ec2-user@ip-172-31-21-145 ~]$ getent ahosts 172.31.21.141
172.31.21.141   STREAM 172.31.21.141
172.31.21.141   DGRAM  
172.31.21.141   RAW    

[ec2-user@ip-172-31-21-145 ~]$ getent ahosts 172.31.21.142
172.31.21.142   STREAM 172.31.21.142
172.31.21.142   DGRAM  
172.31.21.142   RAW    

[ec2-user@ip-172-31-21-145 ~]$ getent ahosts 172.31.21.143
172.31.21.143   STREAM 172.31.21.143
172.31.21.143   DGRAM  
172.31.21.143   RAW    

[ec2-user@ip-172-31-21-145 ~]$ getent ahosts 172.31.21.144
172.31.21.144   STREAM 172.31.21.144
172.31.21.144   DGRAM  
172.31.21.144   RAW    

[ec2-user@ip-172-31-21-145 ~]$ getent ahosts 172.31.21.145
172.31.21.145   STREAM 172.31.21.145
172.31.21.145   DGRAM  
172.31.21.145   RAW   
```

##Nslookup forward and reverse checks
```
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


[ec2-user@ip-172-31-21-145 ~]$ nslookup 172.31.21.142
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
142.21.31.172.in-addr.arpa	name = ip-172-31-21-142.eu-central-1.compute.internal.

Authoritative answers can be found from:

[ec2-user@ip-172-31-21-145 ~]$ nslookup 172.31.21.143
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
143.21.31.172.in-addr.arpa	name = ip-172-31-21-143.eu-central-1.compute.internal.

Authoritative answers can be found from:

[ec2-user@ip-172-31-21-145 ~]$ nslookup 172.31.21.144
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
144.21.31.172.in-addr.arpa	name = ip-172-31-21-144.eu-central-1.compute.internal.

Authoritative answers can be found from:

[ec2-user@ip-172-31-21-145 ~]$ nslookup 172.31.21.145
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
145.21.31.172.in-addr.arpa	name = ip-172-31-21-145.eu-central-1.compute.internal.

Authoritative answers can be found from:
```

#Verify the nscd service is running
```
[ec2-user@ip-172-31-21-145 ~]$ service nscd status
nscd (pid 24378) is running...
```
#Verify the ntpd service is running
```
[ec2-user@ip-172-31-21-145 ~]$ service ntpd status
ntpd (pid  24460) is running...
```











