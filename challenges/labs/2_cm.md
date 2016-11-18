Get the repo file

```
[root@ip-172-31-30-4 tmp]# wget http://archive.cloudera.com/cm5/redhat/6/x86_64/cm/cloudera-manager.repo
--2016-11-18 04:00:47--  http://archive.cloudera.com/cm5/redhat/6/x86_64/cm/cloudera-manager.repo
Resolving archive.cloudera.com... 151.101.12.167
Connecting to archive.cloudera.com|151.101.12.167|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 290
Saving to: “cloudera-manager.repo”

100%[===========================================================================================================>] 290         --.-K/s   in 0s      

2016-11-18 04:00:47 (52.5 MB/s) - “cloudera-manager.repo” saved [290/290]

[root@ip-172-31-30-4 tmp]# mv cloudera-manager.repo /etc/yum.repos.d/

```

```
[root@ip-172-31-30-4 yum.repos.d]# ls /etc/yum.repos.d
cloudera-manager.repo  mysql-community-source.repo  redhat-rhui-client-config.repo  rhel-source.repo
mysql-community.repo   redhat.repo                  redhat-rhui.repo                rhui-load-balancers.conf

```

