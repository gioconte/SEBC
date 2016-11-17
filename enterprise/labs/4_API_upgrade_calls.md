
#API calls

Retrieving API version
```
curl -u admin:admin http://54.93.218.251:7180/api/version
v14
```

Retrieving Cloudera Manager Version
```
[root@localhost tmp]# curl -u admin:admin http://54.93.218.251:7180/api/v14/cm/version
{
  "version" : "5.9.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20161006-1801",
  "gitHash" : "898a5e032c080e18833dfc58180761f6ef2ea351",
  "snapshot" : false
}
```
List all users in cloudera Manager
 
 ```
[root@localhost tmp]# curl -u admin:admin http://54.93.218.251:7180/api/v14/users
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "gioconte",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}
```

Retrieve DB information

```
[root@localhost tmp]# curl -u admin:admin http://54.93.218.251:7180/api/v14/cm/scmDbInfo
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
```
