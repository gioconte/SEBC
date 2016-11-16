```
[ec2-user@ip-172-31-22-224 ~]$ beeline
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Beeline version 1.1.0-cdh5.8.2 by Apache Hive
beeline> !connect jdbc:hive2://172.31.19.14:10000/default;principal=hive/ip-172-31-19-14.eu-central-1.compute.internal@MOVIRI.COM 
scan complete in 3ms
Connecting to jdbc:hive2://172.31.19.14:10000/default;principal=hive/ip-172-31-19-14.eu-central-1.compute.internal@MOVIRI.COM
Enter username for jdbc:hive2://172.31.19.14:10000/default;principal=hive/ip-172-31-19-14.eu-central-1.compute.internal@MOVIRI.COM: gioconte
Enter password for jdbc:hive2://172.31.19.14:10000/default;principal=hive/ip-172-31-19-14.eu-central-1.compute.internal@MOVIRI.COM: ********
Connected to: Apache Hive (version 1.1.0-cdh5.8.2)
Driver: Hive JDBC (version 1.1.0-cdh5.8.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://172.31.19.14:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20161116174444_420853c4-c1f1-4380-b5cd-3ba821e1bce1): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161116174444_420853c4-c1f1-4380-b5cd-3ba821e1bce1); Time taken: 0.707 seconds
INFO  : Executing command(queryId=hive_20161116174444_420853c4-c1f1-4380-b5cd-3ba821e1bce1): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161116174444_420853c4-c1f1-4380-b5cd-3ba821e1bce1); Time taken: 0.258 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (1.309 seconds)
```

Create Role
```
0: jdbc:hive2://172.31.19.14:10000/default> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20161116174646_8237c61f-310f-46de-a644-22b1d59aed62): CREATE ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161116174646_8237c61f-310f-46de-a644-22b1d59aed62); Time taken: 0.083 seconds
INFO  : Executing command(queryId=hive_20161116174646_8237c61f-310f-46de-a644-22b1d59aed62): CREATE ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161116174646_8237c61f-310f-46de-a644-22b1d59aed62); Time taken: 0.441 seconds
INFO  : OK
No rows affected (0.533 seconds)
```
grant on server
```
0: jdbc:hive2://172.31.19.14:10000/default> GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20161116174646_f34e9d41-ff7d-4925-a434-f8ea0b0ef94d): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161116174646_f34e9d41-ff7d-4925-a434-f8ea0b0ef94d); Time taken: 0.095 seconds
INFO  : Executing command(queryId=hive_20161116174646_f34e9d41-ff7d-4925-a434-f8ea0b0ef94d): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161116174646_f34e9d41-ff7d-4925-a434-f8ea0b0ef94d); Time taken: 0.091 seconds
INFO  : OK
No rows affected (0.216 seconds)
0: jdbc:hive2://172.31.19.14:10000/default> 
```

grant role to primary group
```
0: jdbc:hive2://172.31.19.14:10000/default> GRANT ROLE sentry_admin TO GROUP gioconte;
INFO  : Compiling command(queryId=hive_20161116174747_70a61a4f-90c0-4596-9b18-985607557a88): GRANT ROLE sentry_admin TO GROUP gioconte
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161116174747_70a61a4f-90c0-4596-9b18-985607557a88); Time taken: 0.067 seconds
INFO  : Executing command(queryId=hive_20161116174747_70a61a4f-90c0-4596-9b18-985607557a88): GRANT ROLE sentry_admin TO GROUP gioconte
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161116174747_70a61a4f-90c0-4596-9b18-985607557a88); Time taken: 0.096 seconds
INFO  : OK
No rows affected (0.172 seconds)
```
Runing show tables
```
0: jdbc:hive2://172.31.19.14:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20161116174747_61daed61-c201-42a5-917a-a66e8b060fe9): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161116174747_61daed61-c201-42a5-917a-a66e8b060fe9); Time taken: 0.056 seconds
INFO  : Executing command(queryId=hive_20161116174747_61daed61-c201-42a5-917a-a66e8b060fe9): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161116174747_61daed61-c201-42a5-917a-a66e8b060fe9); Time taken: 0.126 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.235 seconds)
```
#Creating Linux user on hosts and adding principal

```
[ec2-user@ip-172-31-22-224 ~]$ sudo groupadd selector
[ec2-user@ip-172-31-22-224 ~]$ sudo groupadd inserters
[ec2-user@ip-172-31-22-224 ~]$ sudo useradd -u 1100 -g selector george
[ec2-user@ip-172-31-22-224 ~]$ sudo useradd -u 1200 -g inserters ferdinand
[ec2-user@ip-172-31-22-224 ~]$ 
[ec2-user@ip-172-31-22-224 ~]$ kadmin.local: add_principal george
-bash: kadmin.local:: command not found
[ec2-user@ip-172-31-22-224 ~]$ sudo kadmin.local: add_principal george
sudo: kadmin.local:: command not found
[ec2-user@ip-172-31-22-224 ~]$ sudo /usr/sbin/kadmin.local -q "addprinc george"
Authenticating as principal root/admin@MOVIRI.COM with password.
WARNING: no policy specified for george@MOVIRI.COM; defaulting to no policy
Enter password for principal "george@MOVIRI.COM": 
Re-enter password for principal "george@MOVIRI.COM": 
Principal "george@MOVIRI.COM" created.
[ec2-user@ip-172-31-22-224 ~]$ sudo /usr/sbin/kadmin.local -q "addprinc ferdinand"
Authenticating as principal root/admin@MOVIRI.COM with password.
WARNING: no policy specified for ferdinand@MOVIRI.COM; defaulting to no policy
Enter password for principal "ferdinand@MOVIRI.COM": 
Re-enter password for principal "ferdinand@MOVIRI.COM": 
Principal "ferdinand@MOVIRI.COM" created.
```
