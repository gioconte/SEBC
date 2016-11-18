EC2 instances purchased in Frankfurt region, availability zone: `europe-1b`, Os: `RHEL 6.7` AMI 

ID: `RHEL-6.7_HVM-20160219-x86_64-1-Hourly2-GP2 (ami-cd362ca1)`

Listing public and private IPs for the machines>

```
54.93.61.118, ec2-54-93-61-118.eu-central-1.compute.amazonaws.com, 172.31.17.8
54.93.128.214, ec2-54-93-128-214.eu-central-1.compute.amazonaws.com, 172.31.30.4
54.93.189.169, ec2-54-93-189-169.eu-central-1.compute.amazonaws.com, 172.31.30.7
54.93.188.98, ec2-54-93-188-98.eu-central-1.compute.amazonaws.com, 172.31.30.5
52.59.237.84, ec2-52-59-237-84.eu-central-1.compute.amazonaws.com, 172.31.30.6
```


Listing space on all machines.
```
[ec2-user@ip-172-31-17-8 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       69G  1.7G   64G   3% /
tmpfs           7.3G     0  7.3G   0% /dev/shm

[ec2-user@ip-172-31-30-4 ~]$  df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       69G  1.7G   64G   3% /
tmpfs           7.3G     0  7.3G   0% /dev/shm

[ec2-user@ip-172-31-30-7 ~]$  df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       69G  1.7G   64G   3% /
tmpfs           7.3G     0  7.3G   0% /dev/shm

[ec2-user@ip-172-31-30-5 ~]$  df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       69G  1.7G   64G   3% /
tmpfs           7.3G     0  7.3G   0% /dev/shm

[ec2-user@ip-172-31-30-6 ~]$  df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       69G  1.7G   64G   3% /
tmpfs           7.3G     0  7.3G   0% /dev/shm

```


Launching command `sudo yum repolist enabled`

```
[ec2-user@ip-172-31-17-8 ~]$ sudo yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, security
rhui-REGION-client-config-server-6                                                              

                              | 2.9 kB     00:00     
rhui-REGION-client-config-server-6/primary_db                                                   

                              | 4.0 kB     00:00     
rhui-REGION-rhel-server-releases                                                                

                              | 3.5 kB     00:00     
rhui-REGION-rhel-server-releases/primary_db                                                     

                              |  51 MB     00:00     
rhui-REGION-rhel-server-rh-common                                                               

                              | 3.8 kB     00:00     
rhui-REGION-rhel-server-rh-common/primary_db                                                    

                              |  65 kB     00:00     
repo id                                                  repo name                              

                                               status
rhui-REGION-client-config-server-6                       Red Hat Update Infrastructure 2.0 

Client Configuration Server 6                            3
rhui-REGION-rhel-server-releases                         Red Hat Enterprise Linux Server 6 

(RPMs)                                              18,369
rhui-REGION-rhel-server-rh-common                        Red Hat Enterprise Linux Server 6 RH 

Common (RPMs)                                       129
repolist: 18,501

[ec2-user@ip-172-31-30-4 ~]$ sudo yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, security
rhui-REGION-client-config-server-6                                                              

                              | 2.9 kB     00:00     
rhui-REGION-client-config-server-6/primary_db                                                   

                              | 4.0 kB     00:00     
rhui-REGION-rhel-server-releases                                                                

                              | 3.5 kB     00:00     
rhui-REGION-rhel-server-releases/primary_db                                                     

                              |  51 MB     00:00     
rhui-REGION-rhel-server-rh-common                                                               

                              | 3.8 kB     00:00     
rhui-REGION-rhel-server-rh-common/primary_db                                                    

                              |  65 kB     00:00     
repo id                                                  repo name                              

                                               status
rhui-REGION-client-config-server-6                       Red Hat Update Infrastructure 2.0 

Client Configuration Server 6                            3
rhui-REGION-rhel-server-releases                         Red Hat Enterprise Linux Server 6 

(RPMs)                                              18,369
rhui-REGION-rhel-server-rh-common                        Red Hat Enterprise Linux Server 6 RH 

Common (RPMs)                                       129
repolist: 18,501

ec2-user@ip-172-31-30-7 ~]$ sudo yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, security
rhui-REGION-client-config-server-6                                                              

                              | 2.9 kB     00:00     
rhui-REGION-client-config-server-6/primary_db                                                   

                              | 4.0 kB     00:00     
rhui-REGION-rhel-server-releases                                                                

                              | 3.5 kB     00:00     
rhui-REGION-rhel-server-releases/primary_db                                                     

                              |  51 MB     00:00     
rhui-REGION-rhel-server-rh-common                                                               

                              | 3.8 kB     00:00     
rhui-REGION-rhel-server-rh-common/primary_db                                                    

                              |  65 kB     00:00     
repo id                                                  repo name                              

                                               status
rhui-REGION-client-config-server-6                       Red Hat Update Infrastructure 2.0 

Client Configuration Server 6                            3
rhui-REGION-rhel-server-releases                         Red Hat Enterprise Linux Server 6 

(RPMs)                                              18,369
rhui-REGION-rhel-server-rh-common                        Red Hat Enterprise Linux Server 6 RH 

Common (RPMs)                                       129
repolist: 18,501


[ec2-user@ip-172-31-30-5 ~]$ sudo yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, security
rhui-REGION-client-config-server-6                                                              

                              | 2.9 kB     00:00     
rhui-REGION-client-config-server-6/primary_db                                                   

                              | 4.0 kB     00:00     
rhui-REGION-rhel-server-releases                                                                

                              | 3.5 kB     00:00     
rhui-REGION-rhel-server-releases/primary_db                                                     

                              |  51 MB     00:00     
rhui-REGION-rhel-server-rh-common                                                               

                              | 3.8 kB     00:00     
rhui-REGION-rhel-server-rh-common/primary_db                                                    

                              |  65 kB     00:00     
repo id                                                  repo name                              

                                               status
rhui-REGION-client-config-server-6                       Red Hat Update Infrastructure 2.0 

Client Configuration Server 6                            3
rhui-REGION-rhel-server-releases                         Red Hat Enterprise Linux Server 6 

(RPMs)                                              18,369
rhui-REGION-rhel-server-rh-common                        Red Hat Enterprise Linux Server 6 RH 

Common (RPMs)                                       129
repolist: 18,501


[ec2-user@ip-172-31-30-6 ~]$ sudo yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, security
rhui-REGION-client-config-server-6                                                              

                              | 2.9 kB     00:00     
rhui-REGION-client-config-server-6/primary_db                                                   

                              | 4.0 kB     00:00     
rhui-REGION-rhel-server-releases                                                                

                              | 3.5 kB     00:00     
rhui-REGION-rhel-server-releases/primary_db                                                     

                              |  51 MB     00:00     
rhui-REGION-rhel-server-rh-common                                                               

                              | 3.8 kB     00:00     
rhui-REGION-rhel-server-rh-common/primary_db                                                    

                              |  65 kB     00:00     
repo id                                                  repo name                              

                                               status
rhui-REGION-client-config-server-6                       Red Hat Update Infrastructure 2.0 

Client Configuration Server 6                            3
rhui-REGION-rhel-server-releases                         Red Hat Enterprise Linux Server 6 

(RPMs)                                              18,369
rhui-REGION-rhel-server-rh-common                        Red Hat Enterprise Linux Server 6 RH 

Common (RPMs)                                       129
repolist: 18,501

```
