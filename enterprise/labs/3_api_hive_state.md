Here to code to check Hive Status

```
[root@localhost tmp]# curl -u admin:admin 'http://54.93.218.251:7180/api/v13/clusters/gioconte/services/hive/'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-22-224.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-22-224.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
}
```


Stop and start hive service.
```
[root@localhost tmp]# curl -u admin:admin -X POST 'http://54.93.218.251:7180/api/v13/clusters/gioconte/services/hive/commands/stop'
{
  "id" : 475,
  "name" : "Stop",
  "startTime" : "2016-11-16T11:05:23.171Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}[root@localhost tmp]# curl -u admin:admin -X POST 'http://54.93.218.251:7180/api/v13/clusters/gioconte/services/hive/commands/start'
{
  "id" : 478,
  "name" : "Start",
  "startTime" : "2016-11-16T11:05:27.660Z",
  "endTime" : "2016-11-16T11:05:27.660Z",
  "active" : false,
  "success" : false,
  "resultMessage" : "Command Start is not currently available for execution.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}```
