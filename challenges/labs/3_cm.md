```
mysql> grant all on hive.* TO 'hive'@'%' IDENTIFIED BY 'password';
Query OK, 0 rows affected (0.00 sec)

mysql> grant all on hue.* TO 'hue'@'%' IDENTIFIED BY 'password';
Query OK, 0 rows affected (0.00 sec)

mysql> grant all on oozie.* TO 'oozie'@'%' IDENTIFIED BY 'password'
    -> ;


mysql> grant all on rman.* TO 'rman'@'%' IDENTIFIED BY 'password';
Query OK, 0 rows affected (0.00 sec)

mysql> grant all on sentry.* TO 'sentry'@'%' IDENTIFIED BY 'password';
Query OK, 0 rows affected (0.00 sec)
```
```
mysql> SHOW GRANTS FOR rman;
+-----------------------------------------------------------------------------------------------------+
| Grants for rman@%                                                                                   |
+-----------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'rman'@'%' IDENTIFIED BY PASSWORD '*2470C0C06DEE42FD1618BB99005ADCA2EC9D1E19' |
| GRANT ALL PRIVILEGES ON `rman`.* TO 'rman'@'%'                                                      |
+-----------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)

mysql> SHOW GRANTS FOR hive;
+-----------------------------------------------------------------------------------------------------+
| Grants for hive@%                                                                                   |
+-----------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'hive'@'%' IDENTIFIED BY PASSWORD '*2470C0C06DEE42FD1618BB99005ADCA2EC9D1E19' |
| GRANT ALL PRIVILEGES ON `hive`.* TO 'hive'@'%'                                                      |
+-----------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)
```


Creating user directories in hdfs
```
[root@ip-172-31-30-5 tmp]# sudo -u hdfs hdfs dfs -chown bavaria /user/bavaria
[root@ip-172-31-30-5 tmp]# sudo -u hdfs hdfs dfs -mkdir -p /user/saxony
[root@ip-172-31-30-5 tmp]# sudo -u hdfs hdfs dfs -chown saxony /user/saxony
[root@ip-172-31-30-5 tmp]# sudo -u hdfs hdfs dfs -ls /user
Found 8 items
drwxr-xr-x   - admin   admin               0 2016-11-18 05:43 /user/admin
drwxr-xr-x   - bavaria supergroup          0 2016-11-18 05:41 /user/bavaria
drwxr-xr-x   - hdfs    supergroup          0 2016-11-18 05:43 /user/hdfs
drwxrwxrwx   - mapred  hadoop              0 2016-11-18 05:36 /user/history
drwxrwxr-t   - hive    hive                0 2016-11-18 05:37 /user/hive
drwxrwxr-x   - hue     hue                 0 2016-11-18 05:38 /user/hue
drwxrwxr-x   - oozie   oozie               0 2016-11-18 05:38 /user/oozie
drwxr-xr-x   - saxony  supergroup          0 2016-11-18 05:47 /user/saxony

```

API CALL

```
{
  "items" : [ {
    "hostId" : "i-ab4c7f17",
    "ipAddress" : "172.31.17.8",
    "hostname" : "ip-172-31-17-8.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-30-4.eu-central-1.compute.internal:7180/cmf/hostRedirect/i-ab4c7f17",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "i-c14e7d7d",
    "ipAddress" : "172.31.30.4",
    "hostname" : "ip-172-31-30-4.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-30-4.eu-central-1.compute.internal:7180/cmf/hostRedirect/i-c14e7d7d",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "i-c64e7d7a",
    "ipAddress" : "172.31.30.5",
    "hostname" : "ip-172-31-30-5.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-30-4.eu-central-1.compute.internal:7180/cmf/hostRedirect/i-c64e7d7a",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "i-c74e7d7b",
    "ipAddress" : "172.31.30.6",
    "hostname" : "ip-172-31-30-6.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-30-4.eu-central-1.compute.internal:7180/cmf/hostRedirect/i-c74e7d7b",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "i-c44e7d78",
    "ipAddress" : "172.31.30.7",
    "hostname" : "ip-172-31-30-7.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-30-4.eu-central-1.compute.internal:7180/cmf/hostRedirect/i-c44e7d78",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  } ]
}
```
