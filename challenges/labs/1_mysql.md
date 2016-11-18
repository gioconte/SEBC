installing MySQL REPO:

```
[root@ip-172-31-17-8 tmp]# wget https://dev.mysql.com/get/mysql57-community-release-el6-

9.noarch.rpm
--2016-11-18 03:28:45--  https://dev.mysql.com/get/mysql57-community-release-el6-9.noarch.rpm
Resolving dev.mysql.com... 137.254.60.11
Connecting to dev.mysql.com|137.254.60.11|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: http://repo.mysql.com//mysql57-community-release-el6-9.noarch.rpm [following]
--2016-11-18 03:28:46--  http://repo.mysql.com//mysql57-community-release-el6-9.noarch.rpm
Resolving repo.mysql.com... 104.108.47.193
Connecting to repo.mysql.com|104.108.47.193|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9216 (9.0K) [application/x-redhat-package-manager]
Saving to: “mysql57-community-release-el6-9.noarch.rpm”

100%[==========================================================================================

=================>] 9,216       --.-K/s   in 0s      

2016-11-18 03:28:47 (521 MB/s) - “mysql57-community-release-el6-9.noarch.rpm” saved [9216/9216]



[root@ip-172-31-17-8 tmp]# rpm -ivh mysql57-community-release-el6-9.noarch.rpm
warning: mysql57-community-release-el6-9.noarch.rpm: Header V3 DSA/SHA1 Signature, key ID 

5072e1f5: NOKEY
Preparing...                ########################################### [100%]
   1:mysql57-community-relea########################################### [100%]
```

Changing enabled flag on mysql version 5.6 to install the requested version

```
[root@ip-172-31-30-6 ec2-user]# vi /etc/yum.repos.d/mysql-community.repo
```


Installing Mysql Community Server>

```
[root@ip-172-31-17-8 tmp]# sudo yum install mysql -y mysql-community-server
Loaded plugins: amazon-id, rhui-lb, security
Setting up Install Process
mysql-connectors-community                                                                      

                              | 2.5 kB     00:00     
mysql-connectors-community/primary_db                                                           

                              |  11 kB     00:00     
mysql-tools-community                                                                           

                              | 2.5 kB     00:00     
mysql-tools-community/primary_db                                                                

                              |  32 kB     00:00     
mysql56-community                                                                               

                              | 2.5 kB     00:00     
mysql56-community/primary_db                                                                    

                              | 168 kB     00:00     
Package mysql is obsoleted by mysql-community-client, trying to install mysql-community-

client-5.6.34-2.el6.x86_64 instead
Resolving Dependencies
--> Running transaction check
---> Package mysql-community-client.x86_64 0:5.6.34-2.el6 will be installed
--> Processing Dependency: mysql-community-libs(x86-64) >= 5.6.10 for package: mysql-

community-client-5.6.34-2.el6.x86_64
---> Package mysql-community-server.x86_64 0:5.6.34-2.el6 will be installed
--> Processing Dependency: mysql-community-common(x86-64) = 5.6.34-2.el6 for package: mysql-

community-server-5.6.34-2.el6.x86_64
--> Running transaction check
---> Package mysql-community-common.x86_64 0:5.6.34-2.el6 will be installed
---> Package mysql-community-libs.x86_64 0:5.6.34-2.el6 will be obsoleting
---> Package mysql-libs.x86_64 0:5.1.73-5.el6_6 will be obsoleted
--> Processing Dependency: libmysqlclient.so.16()(64bit) for package: 2:postfix-2.6.6-

6.el6_5.x86_64
--> Processing Dependency: libmysqlclient.so.16(libmysqlclient_16)(64bit) for package: 

2:postfix-2.6.6-6.el6_5.x86_64
--> Running transaction check
---> Package mysql-community-libs-compat.x86_64 0:5.6.34-2.el6 will be obsoleting
---> Package postfix.x86_64 2:2.6.6-6.el6_5 will be updated
---> Package postfix.x86_64 2:2.6.6-6.el6_7.1 will be an update
--> Finished Dependency Resolution

Dependencies Resolved

===============================================================================================

======================================================
 Package                                   Arch                 Version                         

Repository                                      Size
===============================================================================================

======================================================
Installing:
 mysql-community-client                    x86_64               5.6.34-2.el6                    

mysql56-community                               18 M
 mysql-community-libs                      x86_64               5.6.34-2.el6                    

mysql56-community                              1.9 M
     replacing  mysql-libs.x86_64 5.1.73-5.el6_6
 mysql-community-libs-compat               x86_64               5.6.34-2.el6                    

mysql56-community                              1.6 M
     replacing  mysql-libs.x86_64 5.1.73-5.el6_6
 mysql-community-server                    x86_64               5.6.34-2.el6                    

mysql56-community                               54 M
Installing for dependencies:
 mysql-community-common                    x86_64               5.6.34-2.el6                    

mysql56-community                              308 k
Updating for dependencies:
 postfix                                   x86_64               2:2.6.6-6.el6_7.1               

rhui-REGION-rhel-server-releases               2.0 M

Transaction Summary
===============================================================================================

======================================================
Install       5 Package(s)
Upgrade       1 Package(s)

Total download size: 78 M
Downloading Packages:
(1/6): mysql-community-client-5.6.34-2.el6.x86_64.rpm                                           

                              |  18 MB     00:00     
(2/6): mysql-community-common-5.6.34-2.el6.x86_64.rpm                                           

                              | 308 kB     00:00     
(3/6): mysql-community-libs-5.6.34-2.el6.x86_64.rpm                                             

                              | 1.9 MB     00:00     
(4/6): mysql-community-libs-compat-5.6.34-2.el6.x86_64.rpm                                      

                              | 1.6 MB     00:00     
(5/6): mysql-community-server-5.6.34-2.el6.x86_64.rpm                                           

                              |  54 MB     00:00     
(6/6): postfix-2.6.6-6.el6_7.1.x86_64.rpm                                                       

                              | 2.0 MB     00:00     
-----------------------------------------------------------------------------------------------

------------------------------------------------------
Total                                                                                           

                      52 MB/s |  78 MB     00:01     
warning: rpmts_HdrFromFdno: Header V3 DSA/SHA1 Signature, key ID 5072e1f5: NOKEY
Retrieving key from file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
Importing GPG key 0x5072E1F5:
 Userid : MySQL Release Engineering <mysql-build@oss.oracle.com>
 Package: mysql57-community-release-el6-9.noarch (installed)
 From   : /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Installing : mysql-community-common-5.6.34-2.el6.x86_64                                       

                                                 1/8 
  Installing : mysql-community-libs-5.6.34-2.el6.x86_64                                         

                                                 2/8 
  Installing : mysql-community-libs-compat-5.6.34-2.el6.x86_64                                  

                                                 3/8 
  Installing : mysql-community-client-5.6.34-2.el6.x86_64                                       

                                                 4/8 
  Installing : mysql-community-server-5.6.34-2.el6.x86_64                                       

                                                 5/8 
  Updating   : 2:postfix-2.6.6-6.el6_7.1.x86_64                                                 

                                                 6/8 
  Cleanup    : 2:postfix-2.6.6-6.el6_5.x86_64                                                   

                                                 7/8 
  Erasing    : mysql-libs-5.1.73-5.el6_6.x86_64                                                 

                                                 8/8 
  Verifying  : mysql-community-common-5.6.34-2.el6.x86_64                                       

                                                 1/8 
  Verifying  : mysql-community-libs-5.6.34-2.el6.x86_64                                         

                                                 2/8 
  Verifying  : mysql-community-libs-compat-5.6.34-2.el6.x86_64                                  

                                                 3/8 
  Verifying  : mysql-community-server-5.6.34-2.el6.x86_64                                       

                                                 4/8 
  Verifying  : 2:postfix-2.6.6-6.el6_7.1.x86_64                                                 

                                                 5/8 
  Verifying  : mysql-community-client-5.6.34-2.el6.x86_64                                       

                                                 6/8 
  Verifying  : mysql-libs-5.1.73-5.el6_6.x86_64                                                 

                                                 7/8 
  Verifying  : 2:postfix-2.6.6-6.el6_5.x86_64                                                   

                                                 8/8 

Installed:
  mysql-community-client.x86_64 0:5.6.34-2.el6    mysql-community-libs.x86_64 0:5.6.34-2.el6    

mysql-community-libs-compat.x86_64 0:5.6.34-2.el6   
  mysql-community-server.x86_64 0:5.6.34-2.el6   

Dependency Installed:
  mysql-community-common.x86_64 0:5.6.34-2.el6                                                  

                                                     

Dependency Updated:
  postfix.x86_64 2:2.6.6-6.el6_7.1                                                              

                                                     

Replaced:
  mysql-libs.x86_64 0:5.1.73-5.el6_6                                                            

                                                     

Complete!

```



Going to change `my.cnf` file to put the right configurations with the following:
```
[mysqld]
transaction-isolation = READ-COMMITTED

key_buffer = 16M
key_buffer_size = 32M
max_allowed_packet = 32M
thread_stack = 256K
thread_cache_size = 64
query_cache_limit = 8M
query_cache_size = 64M
query_cache_type = 1

max_connections = 550

log_bin=/var/lib/mysql/mysql_binary_log

# For MySQL version 5.1.8 or later. Comment out binlog_format for older versions.
#binlog_format = mixed

read_buffer_size = 2M
read_rnd_buffer_size = 16M
sort_buffer_size = 8M
join_buffer_size = 8M

# InnoDB settings
innodb_file_per_table = 1
innodb_flush_log_at_trx_commit  = 2
innodb_log_buffer_size = 64M
innodb_buffer_pool_size = 4G
innodb_thread_concurrency = 8
innodb_flush_method = O_DIRECT
innodb_log_file_size = 512M

[mysqld_safe]
log-error=/var/log/mysqld.log
pid-file=/var/run/mysqld/mysqld.pid

sql_mode=STRICT_ALL_TABLES
```

Starting MySQL server:
```
[root@ip-172-31-17-8 tmp]# service mysqld start
Initializing MySQL database:  2016-11-18 03:43:06 0 [Warning] Using unique option prefix key_buffer instead of key_buffer_size is deprecated and will be removed in a future release. Please use the full name instead.
2016-11-18 03:43:06 0 [Warning] TIMESTAMP with implicit DEFAULT value is deprecated. Please use --explicit_defaults_for_timestamp server option (see documentation for more details).
2016-11-18 03:43:06 0 [Note] Ignoring --secure-file-priv value as server is running with --bootstrap.
2016-11-18 03:43:06 0 [Note] /usr/sbin/mysqld (mysqld 5.6.34-log) starting as process 24736 ...
2016-11-18 03:43:06 24736 [Note] InnoDB: Using atomics to ref count buffer pool pages
2016-11-18 03:43:06 24736 [Note] InnoDB: The InnoDB memory heap is disabled
2016-11-18 03:43:06 24736 [Note] InnoDB: Mutexes and rw_locks use GCC atomic builtins
2016-11-18 03:43:06 24736 [Note] InnoDB: Memory barrier is not used
2016-11-18 03:43:06 24736 [Note] InnoDB: Compressed tables use zlib 1.2.3
2016-11-18 03:43:06 24736 [Note] InnoDB: Using Linux native AIO
2016-11-18 03:43:06 24736 [Note] InnoDB: Using CPU crc32 instructions
2016-11-18 03:43:06 24736 [Note] InnoDB: Initializing buffer pool, size = 4.0G
2016-11-18 03:43:07 24736 [Note] InnoDB: Completed initialization of buffer pool
2016-11-18 03:43:07 24736 [Note] InnoDB: The first specified data file ./ibdata1 did not exist: a new database to be created!
2016-11-18 03:43:07 24736 [Note] InnoDB: Setting file ./ibdata1 size to 12 MB
2016-11-18 03:43:07 24736 [Note] InnoDB: Database physically writes the file full: wait...
2016-11-18 03:43:09 24736 [Note] InnoDB: Setting log file ./ib_logfile101 size to 512 MB
InnoDB: Progress in MB: 100 200 300 400 500
2016-11-18 03:44:22 24736 [Note] InnoDB: Setting log file ./ib_logfile1 size to 512 MB
InnoDB: Progress in MB: 100 200 300 400 500
2016-11-18 03:45:56 24736 [Note] InnoDB: Renaming log file ./ib_logfile101 to ./ib_logfile0
2016-11-18 03:45:56 24736 [Warning] InnoDB: New log files created, LSN=45781
2016-11-18 03:45:56 24736 [Note] InnoDB: Doublewrite buffer not found: creating new
2016-11-18 03:45:56 24736 [Note] InnoDB: Doublewrite buffer created
2016-11-18 03:45:56 24736 [Note] InnoDB: 128 rollback segment(s) are active.
2016-11-18 03:45:56 24736 [Warning] InnoDB: Creating foreign key constraint system tables.
2016-11-18 03:45:56 24736 [Note] InnoDB: Foreign key constraint system tables created
2016-11-18 03:45:56 24736 [Note] InnoDB: Creating tablespace and datafile system tables.
2016-11-18 03:45:56 24736 [Note] InnoDB: Tablespace and datafile system tables created.
2016-11-18 03:45:56 24736 [Note] InnoDB: Waiting for purge to start
2016-11-18 03:45:56 24736 [Note] InnoDB: 5.6.34 started; log sequence number 0
2016-11-18 03:45:58 24736 [Note] Binlog end
2016-11-18 03:45:58 24736 [Note] InnoDB: FTS optimize thread exiting.
2016-11-18 03:45:58 24736 [Note] InnoDB: Starting shutdown...
2016-11-18 03:45:59 24736 [Note] InnoDB: Shutdown completed; log sequence number 1625977


2016-11-18 03:45:59 0 [Warning] Using unique option prefix key_buffer instead of key_buffer_size is deprecated and will be removed in a future release. Please use the full name instead.
2016-11-18 03:45:59 0 [Warning] TIMESTAMP with implicit DEFAULT value is deprecated. Please use --explicit_defaults_for_timestamp server option (see documentation for more details).
2016-11-18 03:45:59 0 [Note] Ignoring --secure-file-priv value as server is running with --bootstrap.
2016-11-18 03:45:59 0 [Note] /usr/sbin/mysqld (mysqld 5.6.34-log) starting as process 24762 ...
2016-11-18 03:45:59 24762 [Note] InnoDB: Using atomics to ref count buffer pool pages
2016-11-18 03:45:59 24762 [Note] InnoDB: The InnoDB memory heap is disabled
2016-11-18 03:45:59 24762 [Note] InnoDB: Mutexes and rw_locks use GCC atomic builtins
2016-11-18 03:45:59 24762 [Note] InnoDB: Memory barrier is not used
2016-11-18 03:45:59 24762 [Note] InnoDB: Compressed tables use zlib 1.2.3
2016-11-18 03:45:59 24762 [Note] InnoDB: Using Linux native AIO
2016-11-18 03:45:59 24762 [Note] InnoDB: Using CPU crc32 instructions
2016-11-18 03:45:59 24762 [Note] InnoDB: Initializing buffer pool, size = 4.0G
2016-11-18 03:46:00 24762 [Note] InnoDB: Completed initialization of buffer pool
2016-11-18 03:46:00 24762 [Note] InnoDB: Highest supported file format is Barracuda.
2016-11-18 03:46:00 24762 [Note] InnoDB: 128 rollback segment(s) are active.
2016-11-18 03:46:00 24762 [Note] InnoDB: Waiting for purge to start
2016-11-18 03:46:00 24762 [Note] InnoDB: 5.6.34 started; log sequence number 1625977
2016-11-18 03:46:00 24762 [Note] Binlog end
2016-11-18 03:46:00 24762 [Note] InnoDB: FTS optimize thread exiting.
2016-11-18 03:46:00 24762 [Note] InnoDB: Starting shutdown...
2016-11-18 03:46:02 24762 [Note] InnoDB: Shutdown completed; log sequence number 1625987




PLEASE REMEMBER TO SET A PASSWORD FOR THE MySQL root USER !
To do so, start the server, then issue the following commands:

  /usr/bin/mysqladmin -u root password 'new-password'
  /usr/bin/mysqladmin -u root -h ip-172-31-17-8.eu-central-1.compute.internal password 'new-password'

Alternatively you can run:

  /usr/bin/mysql_secure_installation

which will also give you the option of removing the test
databases and anonymous user created by default.  This is
strongly recommended for production servers.

See the manual for more instructions.

Please report any problems at http://bugs.mysql.com/

The latest information about MySQL is available on the web at

  http://www.mysql.com

Support MySQL by buying support/licenses at http://shop.mysql.com

Note: new default config file not created.
Please make sure your config file is current

WARNING: Default config file /etc/my.cnf exists on the system
This file will be read by default by the MySQL server
If you do not want to use this, either remove it, or use the
--defaults-file argument to mysqld_safe when starting the server

                                                           [  OK  ]
Starting mysqld: 
```


Adding secure installation and removing test tables:


[root@ip-172-31-17-8 tmp]# /usr/bin/mysql_secure_installation



NOTE: RUNNING ALL PARTS OF THIS SCRIPT IS RECOMMENDED FOR ALL MySQL
      SERVERS IN PRODUCTION USE!  PLEASE READ EACH STEP CAREFULLY!

In order to log into MySQL to secure it, we'll need the current
password for the root user.  If you've just installed MySQL, and
you haven't set the root password yet, the password will be blank,
so you should just press enter here.

Enter current password for root (enter for none): 
OK, successfully used password, moving on...

Setting the root password ensures that nobody can log into the MySQL
root user without the proper authorisation.

Set root password? [Y/n] Y
New password: 
Re-enter new password: 
Password updated successfully!
Reloading privilege tables..
 ... Success!


By default, a MySQL installation has an anonymous user, allowing anyone
to log into MySQL without having to have a user account created for
them.  This is intended only for testing, and to make the installation
go a bit smoother.  You should remove them before moving into a
production environment.

Remove anonymous users? [Y/n] Y
 ... Success!

Normally, root should only be allowed to connect from 'localhost'.  This
ensures that someone cannot guess at the root password from the network.

Disallow root login remotely? [Y/n] n
 ... skipping.

By default, MySQL comes with a database named 'test' that anyone can
access.  This is also intended only for testing, and should be removed
before moving into a production environment.

Remove test database and access to it? [Y/n] Y
 - Dropping test database...
ERROR 1008 (HY000) at line 1: Can't drop database 'test'; database doesn't exist
 ... Failed!  Not critical, keep moving...
 - Removing privileges on test database...
 ... Success!

Reloading the privilege tables will ensure that all changes made so far
will take effect immediately.

Reload privilege tables now? [Y/n] Y
 ... Success!




All done!  If you've completed all of the above steps, your MySQL
installation should now be secure.

Thanks for using MySQL!


Cleaning up...
```

```


Installing JDBC Connector on all nodes:

```
[root@ip-172-31-30-5 tmp]# tar zxvf mysql-connector-java-5.1.40.tar.gz
mysql-connector-java-5.1.40/
mysql-connector-java-5.1.40/docs/
mysql-connector-java-5.1.40/src/
mysql-connector-java-5.1.40/src/com/
mysql-connector-java-5.1.40/src/com/mysql/
mysql-connector-java-5.1.40/src/com/mysql/fabric/
mysql-connector-java-5.1.40/src/com/mysql/fabric/hibernate/
mysql-connector-java-5.1.40/src/com/mysql/fabric/jdbc/
mysql-connector-java-5.1.40/src/com/mysql/fabric/proto/
mysql-connector-java-5.1.40/src/com/mysql/fabric/proto/xmlrpc/
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/base/
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/exceptions/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/authentication/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/configs/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/integration/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/integration/c3p0/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/integration/jboss/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/interceptors/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jmx/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/log/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/profiler/
mysql-connector-java-5.1.40/src/com/mysql/jdbc/util/
mysql-connector-java-5.1.40/src/demo/
mysql-connector-java-5.1.40/src/demo/fabric/
mysql-connector-java-5.1.40/src/demo/fabric/resources/
mysql-connector-java-5.1.40/src/demo/fabric/resources/com/
mysql-connector-java-5.1.40/src/demo/fabric/resources/com/mysql/
mysql-connector-java-5.1.40/src/demo/fabric/resources/com/mysql/fabric/
mysql-connector-java-5.1.40/src/demo/fabric/resources/com/mysql/fabric/demo/
mysql-connector-java-5.1.40/src/doc/
mysql-connector-java-5.1.40/src/doc/sources/
mysql-connector-java-5.1.40/src/lib/
mysql-connector-java-5.1.40/src/org/
mysql-connector-java-5.1.40/src/org/gjt/
mysql-connector-java-5.1.40/src/org/gjt/mm/
mysql-connector-java-5.1.40/src/org/gjt/mm/mysql/
mysql-connector-java-5.1.40/src/testsuite/
mysql-connector-java-5.1.40/src/testsuite/fabric/
mysql-connector-java-5.1.40/src/testsuite/fabric/jdbc/
mysql-connector-java-5.1.40/src/testsuite/perf/
mysql-connector-java-5.1.40/src/testsuite/regression/
mysql-connector-java-5.1.40/src/testsuite/regression/jdbc4/
mysql-connector-java-5.1.40/src/testsuite/regression/jdbc42/
mysql-connector-java-5.1.40/src/testsuite/simple/
mysql-connector-java-5.1.40/src/testsuite/simple/jdbc4/
mysql-connector-java-5.1.40/src/testsuite/simple/jdbc42/
mysql-connector-java-5.1.40/src/testsuite/ssl-test-certs/
mysql-connector-java-5.1.40/CHANGES
mysql-connector-java-5.1.40/COPYING
mysql-connector-java-5.1.40/README
mysql-connector-java-5.1.40/README.txt
mysql-connector-java-5.1.40/build.xml
mysql-connector-java-5.1.40/docs/README.txt
mysql-connector-java-5.1.40/docs/connector-j.html
mysql-connector-java-5.1.40/docs/connector-j.pdf
mysql-connector-java-5.1.40/mysql-connector-java-5.1.40-bin.jar
mysql-connector-java-5.1.40/src/com/mysql/fabric/FabricCommunicationException.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/FabricConnection.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/FabricStateResponse.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/HashShardMapping.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/RangeShardMapping.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/Response.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/Server.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/ServerGroup.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/ServerMode.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/ServerRole.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/ShardIndex.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/ShardMapping.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/ShardMappingFactory.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/ShardTable.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/ShardingType.java
mysql-connector-java-

5.1.40/src/com/mysql/fabric/hibernate/FabricMultiTenantConnectionProvider.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/jdbc/ErrorReportingExceptionInterceptor.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/jdbc/FabricMySQLConnection.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/jdbc/FabricMySQLConnectionProperties.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/jdbc/FabricMySQLConnectionProxy.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/jdbc/FabricMySQLDataSource.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/jdbc/FabricMySQLDriver.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/jdbc/JDBC4FabricMySQLConnection.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/jdbc/JDBC4FabricMySQLConnectionProxy.java
mysql-connector-java-

5.1.40/src/com/mysql/fabric/proto/xmlrpc/AuthenticatedXmlRpcMethodCaller.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/proto/xmlrpc/DigestAuthentication.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/proto/xmlrpc/InternalXmlRpcMethodCaller.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/proto/xmlrpc/ResultSetParser.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/proto/xmlrpc/XmlRpcClient.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/proto/xmlrpc/XmlRpcMethodCaller.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/Client.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/base/Array.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/base/Data.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/base/Fault.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/base/Member.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/base/MethodCall.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/base/MethodResponse.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/base/Param.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/base/Params.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/base/ResponseParser.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/base/Struct.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/base/Value.java
mysql-connector-java-5.1.40/src/com/mysql/fabric/xmlrpc/exceptions/MySQLFabricException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/AbandonedConnectionCleanupThread.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/AssertionFailedException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/AuthenticationPlugin.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/BalanceStrategy.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/BestResponseTimeBalanceStrategy.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Blob.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/BlobFromLocator.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Buffer.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/BufferRow.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ByteArrayRow.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/CacheAdapter.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/CacheAdapterFactory.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/CachedResultSetMetaData.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/CallableStatement.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/CharsetMapping.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Charsets.properties
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Clob.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/CommunicationsException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/CompressedInputStream.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Connection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ConnectionFeatureNotAvailableException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ConnectionGroup.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ConnectionGroupManager.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ConnectionImpl.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ConnectionLifecycleInterceptor.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ConnectionProperties.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ConnectionPropertiesImpl.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ConnectionPropertiesTransform.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Constants.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/DatabaseMetaData.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/DatabaseMetaDataUsingInfoSchema.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/DocsConnectionPropsHelper.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Driver.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/EscapeProcessor.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/EscapeProcessorResult.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/EscapeTokenizer.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ExceptionInterceptor.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ExportControlled.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Extension.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/FailoverConnectionProxy.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Field.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/IterateBlock.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC42CallableStatement.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC42Helper.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC42PreparedStatement.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC42ResultSet.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC42ServerPreparedStatement.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC42UpdatableResultSet.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4CallableStatement.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4ClientInfoProvider.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4ClientInfoProviderSP.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4CommentClientInfoProvider.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4Connection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4DatabaseMetaData.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4DatabaseMetaDataUsingInfoSchema.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4LoadBalancedMySQLConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4MultiHostMySQLConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4MySQLConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4MysqlSQLXML.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4NClob.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4PreparedStatement.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4PreparedStatementHelper.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4ReplicationMySQLConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4ResultSet.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4ServerPreparedStatement.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/JDBC4UpdatableResultSet.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/LicenseConfiguration.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/LoadBalanceExceptionChecker.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/LoadBalancedAutoCommitInterceptor.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/LoadBalancedConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/LoadBalancedConnectionProxy.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/LoadBalancedMySQLConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/LocalizedErrorMessages.properties
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Messages.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/MiniAdmin.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/MultiHostConnectionProxy.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/MultiHostMySQLConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/MySQLConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/MysqlDataTruncation.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/MysqlDefs.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/MysqlErrorNumbers.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/MysqlIO.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/MysqlParameterMetadata.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/MysqlSavepoint.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/NamedPipeSocketFactory.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/NdbLoadBalanceExceptionChecker.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/NetworkResources.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/NoSubInterceptorWrapper.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/NonRegisteringDriver.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/NonRegisteringReplicationDriver.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/NotImplemented.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/NotUpdatable.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/OperationNotSupportedException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/OutputStreamWatcher.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/PacketTooBigException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ParameterBindings.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/PerConnectionLRUFactory.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/PerVmServerConfigCacheFactory.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/PingTarget.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/PreparedStatement.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ProfilerEventHandlerFactory.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/RandomBalanceStrategy.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ReflectiveStatementInterceptorAdapter.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ReplicationConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ReplicationConnectionGroup.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ReplicationConnectionGroupManager.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ReplicationConnectionProxy.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ReplicationDriver.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ReplicationMySQLConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ResultSetImpl.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ResultSetInternalMethods.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ResultSetMetaData.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ResultSetRow.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/RowData.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/RowDataCursor.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/RowDataDynamic.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/RowDataStatic.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/SQLError.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Security.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/SequentialBalanceStrategy.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/ServerPreparedStatement.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/SingleByteCharsetConverter.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/SocketFactory.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/SocketMetadata.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/SocksProxySocketFactory.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/StandardLoadBalanceExceptionChecker.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/StandardSocketFactory.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Statement.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/StatementImpl.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/StatementInterceptor.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/StatementInterceptorV2.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/StreamingNotifiable.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/StringUtils.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/TimeUtil.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/TimeZoneMapping.properties
mysql-connector-java-5.1.40/src/com/mysql/jdbc/UpdatableResultSet.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Util.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/V1toV2StatementInterceptorAdapter.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/WatchableOutputStream.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/WatchableWriter.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/Wrapper.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/WriterWatcher.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/authentication/MysqlClearPasswordPlugin.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/authentication/MysqlNativePasswordPlugin.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/authentication/MysqlOldPasswordPlugin.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/authentication/Sha256PasswordPlugin.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/configs/3-0-Compat.properties
mysql-connector-java-5.1.40/src/com/mysql/jdbc/configs/5-0-Compat.properties
mysql-connector-java-5.1.40/src/com/mysql/jdbc/configs/clusterBase.properties
mysql-connector-java-5.1.40/src/com/mysql/jdbc/configs/coldFusion.properties
mysql-connector-java-5.1.40/src/com/mysql/jdbc/configs/fullDebug.properties
mysql-connector-java-5.1.40/src/com/mysql/jdbc/configs/maxPerformance.properties
mysql-connector-java-5.1.40/src/com/mysql/jdbc/configs/solarisMaxPerformance.properties
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/DeadlockTimeoutRollbackMarker.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/MySQLDataException.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/exceptions/MySQLIntegrityConstraintViolationException.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/exceptions/MySQLInvalidAuthorizationSpecException.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/exceptions/MySQLNonTransientConnectionException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/MySQLNonTransientException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/MySQLQueryInterruptedException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/MySQLStatementCancelledException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/MySQLSyntaxErrorException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/MySQLTimeoutException.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/exceptions/MySQLTransactionRollbackException.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/exceptions/MySQLTransientConnectionException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/MySQLTransientException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/CommunicationsException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/MySQLDataException.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/MySQLIntegrityConstraintViolationException.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/MySQLInvalidAuthorizationSpecException.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/MySQLNonTransientConnectionException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/MySQLNonTransientException.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/MySQLQueryInterruptedException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/MySQLSyntaxErrorException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/MySQLTimeoutException.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/MySQLTransactionRollbackException.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/MySQLTransientConnectionException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/exceptions/jdbc4/MySQLTransientException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/integration/c3p0/MysqlConnectionTester.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/integration/jboss/ExtendedMysqlExceptionSorter.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/integration/jboss/MysqlValidConnectionChecker.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/interceptors/ResultSetScannerInterceptor.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/interceptors/ServerStatusDiffInterceptor.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/interceptors/SessionAssociationInterceptor.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/CallableStatementWrapper.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/ConnectionWrapper.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/jdbc2/optional/JDBC42CallableStatementWrapper.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/jdbc2/optional/JDBC42PreparedStatementWrapper.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/jdbc2/optional/JDBC4CallableStatementWrapper.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/JDBC4ConnectionWrapper.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/JDBC4MysqlPooledConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/JDBC4MysqlXAConnection.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/jdbc2/optional/JDBC4PreparedStatementWrapper.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/JDBC4StatementWrapper.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/JDBC4SuspendableXAConnection.java
mysql-connector-java-

5.1.40/src/com/mysql/jdbc/jdbc2/optional/MysqlConnectionPoolDataSource.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/MysqlDataSource.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/MysqlDataSourceFactory.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/MysqlPooledConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/MysqlXAConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/MysqlXADataSource.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/MysqlXAException.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/MysqlXid.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/PreparedStatementWrapper.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/StatementWrapper.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/SuspendableXAConnection.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jdbc2/optional/WrapperBase.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jmx/LoadBalanceConnectionGroupManager.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jmx/LoadBalanceConnectionGroupManagerMBean.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jmx/ReplicationGroupManager.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/jmx/ReplicationGroupManagerMBean.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/log/Jdk14Logger.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/log/Log.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/log/LogFactory.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/log/LogUtils.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/log/NullLogger.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/log/Slf4JLogger.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/log/StandardLogger.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/profiler/LoggingProfilerEventHandler.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/profiler/ProfilerEvent.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/profiler/ProfilerEventHandler.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/util/Base64Decoder.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/util/BaseBugReport.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/util/ErrorMappingsDocGenerator.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/util/LRUCache.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/util/PropertiesDocGenerator.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/util/ReadAheadInputStream.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/util/ResultSetUtil.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/util/ServerController.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/util/TimezoneDump.java
mysql-connector-java-5.1.40/src/com/mysql/jdbc/util/VersionFSHierarchyMaker.java
mysql-connector-java-5.1.40/src/demo/fabric/Client1_Fabric.java
mysql-connector-java-5.1.40/src/demo/fabric/Employee.java
mysql-connector-java-5.1.40/src/demo/fabric/EmployeesDataSource.java
mysql-connector-java-5.1.40/src/demo/fabric/EmployeesJdbc.java
mysql-connector-java-5.1.40/src/demo/fabric/HibernateFabric.java
mysql-connector-java-5.1.40/src/demo/fabric/resources/com/mysql/fabric/demo/employee.hbm.xml
mysql-connector-java-5.1.40/src/doc/sources/pom.xml
mysql-connector-java-5.1.40/src/lib/c3p0-0.9.1-pre6.jar
mysql-connector-java-5.1.40/src/lib/c3p0-0.9.1-pre6.src.zip
mysql-connector-java-5.1.40/src/lib/jboss-common-jdbc-wrapper-src.jar
mysql-connector-java-5.1.40/src/lib/jboss-common-jdbc-wrapper.jar
mysql-connector-java-5.1.40/src/lib/slf4j-api-1.6.1.jar
mysql-connector-java-5.1.40/src/org/gjt/mm/mysql/Driver.java
mysql-connector-java-5.1.40/src/testsuite/BaseStatementInterceptor.java
mysql-connector-java-5.1.40/src/testsuite/BaseTestCase.java
mysql-connector-java-5.1.40/src/testsuite/UnreliableSocketFactory.java
mysql-connector-java-5.1.40/src/testsuite/fabric/BaseFabricTestCase.java
mysql-connector-java-5.1.40/src/testsuite/fabric/SetupFabricTestsuite.java
mysql-connector-java-5.1.40/src/testsuite/fabric/TestAdminCommands.java
mysql-connector-java-5.1.40/src/testsuite/fabric/TestDumpCommands.java
mysql-connector-java-5.1.40/src/testsuite/fabric/TestResultSetParser.java
mysql-connector-java-5.1.40/src/testsuite/fabric/TestShardMapping.java
mysql-connector-java-5.1.40/src/testsuite/fabric/TestXmlRpcCore.java
mysql-connector-java-5.1.40/src/testsuite/fabric/jdbc/TestBasicConnection.java
mysql-connector-java-5.1.40/src/testsuite/fabric/jdbc/TestFabricMySQLConnectionSharding.java
mysql-connector-java-5.1.40/src/testsuite/fabric/jdbc/TestHABasics.java
mysql-connector-java-5.1.40/src/testsuite/fabric/jdbc/TestHashSharding.java
mysql-connector-java-5.1.40/src/testsuite/fabric/jdbc/TestRegressions.java
mysql-connector-java-5.1.40/src/testsuite/perf/BasePerfTest.java
mysql-connector-java-5.1.40/src/testsuite/perf/LoadStorePerfTest.java
mysql-connector-java-5.1.40/src/testsuite/perf/RetrievalPerfTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/BlobRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/CachedRowsetTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/CallableStatementRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/CharsetRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/ConnectionRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/DataSourceRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/EscapeProcessorRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/MetaDataRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/MicroPerformanceRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/NumbersRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/PooledConnectionRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/ResultSetRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/StatementRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/StressRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/StringRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/SubqueriesRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/SyntaxRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/UtilsRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/jdbc4/ConnectionRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/jdbc4/ExceptionSubclassesTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/jdbc4/MetaDataRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/jdbc4/StatementRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/regression/jdbc42/StatementRegressionTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/BlobTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/CallableStatementTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/CharsetTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/ConnectionTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/DataSourceTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/DateTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/EscapeProcessingTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/MetadataTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/MiniAdminTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/MultiHostConnectionTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/NumbersTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/ReadOnlyCallableStatementTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/ResultSetTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/SSLTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/ServerControllerTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/SimpleTransformer.java
mysql-connector-java-5.1.40/src/testsuite/simple/SplitDBdotNameTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/StatementsTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/StringUtilsTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/TestBug57662Logger.java
mysql-connector-java-5.1.40/src/testsuite/simple/TestLifecycleInterceptor.java
mysql-connector-java-5.1.40/src/testsuite/simple/TransactionTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/TraversalTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/UpdatabilityTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/UtilsTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/XATest.java
mysql-connector-java-5.1.40/src/testsuite/simple/jdbc4/StatementsTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/jdbc42/ConnectionTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/jdbc42/ResultSetTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/jdbc42/StatementsTest.java
mysql-connector-java-5.1.40/src/testsuite/simple/tb2-data.txt.gz
mysql-connector-java-5.1.40/src/testsuite/ssl-test-certs/ca-cert.pem
mysql-connector-java-5.1.40/src/testsuite/ssl-test-certs/ca-key.pem
mysql-connector-java-5.1.40/src/testsuite/ssl-test-certs/certs_howto.txt
mysql-connector-java-5.1.40/src/testsuite/ssl-test-certs/mykey.pem
mysql-connector-java-5.1.40/src/testsuite/ssl-test-certs/mykey.pub
mysql-connector-java-5.1.40/src/testsuite/ssl-test-certs/server-cert.pem
mysql-connector-java-5.1.40/src/testsuite/ssl-test-certs/server-key.pem
mysql-connector-java-5.1.40/src/testsuite/ssl-test-certs/server-req.pem
mysql-connector-java-5.1.40/src/testsuite/ssl-test-certs/test-cert-store
[root@ip-172-31-30-5 tmp]# sudo mkdir -p /usr/share/java/
[root@ip-172-31-30-5 tmp]# sudo cp mysql-connector-java-5.1.40/mysql-connector-java-5.1.40-

bin.jar /usr/share/java/mysql-connector-java.jar

```



