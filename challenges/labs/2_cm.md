Get the repo file

```
[root@ip-172-31-30-4 tmp]# wget http://archive.cloudera.com/cm5/redhat/6/x86_64/cm/cloudera-

manager.repo
--2016-11-18 04:00:47--  http://archive.cloudera.com/cm5/redhat/6/x86_64/cm/cloudera-

manager.repo
Resolving archive.cloudera.com... 151.101.12.167
Connecting to archive.cloudera.com|151.101.12.167|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 290
Saving to: “cloudera-manager.repo”

100%[==========================================================================================

=================>] 290         --.-K/s   in 0s      

2016-11-18 04:00:47 (52.5 MB/s) - “cloudera-manager.repo” saved [290/290]

[root@ip-172-31-30-4 tmp]# mv cloudera-manager.repo /etc/yum.repos.d/

```

```
[root@ip-172-31-30-4 yum.repos.d]# ls /etc/yum.repos.d
cloudera-manager.repo  mysql-community-source.repo  redhat-rhui-client-config.repo  rhel-

source.repo
mysql-community.repo   redhat.repo                  redhat-rhui.repo                rhui-load-

balancers.conf

```


Installing CM

```
[root@ip-172-31-30-4 yum.repos.d]# yum install cloudera-manager-daemons cloudera-manager-server
Loaded plugins: amazon-id, rhui-lb, security
Setting up Install Process
Resolving Dependencies
--> Running transaction check
---> Package cloudera-manager-daemons.x86_64 0:5.7.4-1.cm574.p0.9.el6 will be installed
---> Package cloudera-manager-server.x86_64 0:5.7.4-1.cm574.p0.9.el6 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

===============================================================================================

======================================================
 Package                                   Arch                    Version                      

             Repository                         Size
===============================================================================================

======================================================
Installing:
 cloudera-manager-daemons                  x86_64                  5.7.4-1.cm574.p0.9.el6       

             cloudera-manager                  538 M
 cloudera-manager-server                   x86_64                  5.7.4-1.cm574.p0.9.el6       

             cloudera-manager                  8.2 k

Transaction Summary
===============================================================================================

======================================================
Install       2 Package(s)

Total download size: 538 M
Installed size: 860 M
Is this ok [y/N]: y
Downloading Packages:
(1/2): cloudera-manager-daemons-5.7.4-1.cm574.p0.9.el6.x86_64.rpm                               

                              | 538 MB     00:07     
(2/2): cloudera-manager-server-5.7.4-1.cm574.p0.9.el6.x86_64.rpm                                

                              | 8.2 kB     00:00     
-----------------------------------------------------------------------------------------------

------------------------------------------------------
Total                                                                                           

                      67 MB/s | 538 MB     00:08     
warning: rpmts_HdrFromFdno: Header V4 DSA/SHA1 Signature, key ID e8f86acd: NOKEY
Retrieving key from https://archive.cloudera.com/cm5/redhat/6/x86_64/cm/RPM-GPG-KEY-cloudera
Importing GPG key 0xE8F86ACD:
 Userid: "Yum Maintainer <webmaster@cloudera.com>"
 From  : https://archive.cloudera.com/cm5/redhat/6/x86_64/cm/RPM-GPG-KEY-cloudera
Is this ok [y/N]: y
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Installing : cloudera-manager-daemons-5.7.4-1.cm574.p0.9.el6.x86_64                           

                                                 1/2 
  Installing : cloudera-manager-server-5.7.4-1.cm574.p0.9.el6.x86_64                            

                                                 2/2 
  Verifying  : cloudera-manager-daemons-5.7.4-1.cm574.p0.9.el6.x86_64                           

                                                 1/2 
  Verifying  : cloudera-manager-server-5.7.4-1.cm574.p0.9.el6.x86_64                            

                                                 2/2 

Installed:
  cloudera-manager-daemons.x86_64 0:5.7.4-1.cm574.p0.9.el6                  cloudera-manager-

server.x86_64 0:5.7.4-1.cm574.p0.9.el6                 

Complete!

```



Adding grant statement for scm.

```
grant all on scm.* TO 'scm'@'172.31.30.4' IDENTIFIED BY 'password';
```


