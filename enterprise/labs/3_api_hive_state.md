<b>Write curl statements that stop, start, and check the current state of your Hive service.</b>
<ul>
<li>Stop HiveServer2<li>
<pre>
curl -u majimenez:cloudera -X POST 'http://ec2-34-251-6-22.eu-west-1.compute.amazonaws.com:7180/api/v12/clusters/majimenez/services/hive/commands/stop'
</pre>
Output<br/>
<pre>
{
  "id" : 376,
  "name" : "Stop",
  "startTime" : "2017-06-07T22:05:04.663Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
</pre>
<li>Start HiveServer2<li>
<pre>
curl -u majimenez:cloudera -X POST 'http://ec2-34-251-6-22.eu-west-1.compute.amazonaws.com:7180/api/v12/clusters/majimenez/services/hive/commands/start'
</pre>
<pre>
{
  "id" : 381,
  "name" : "Start",
  "startTime" : "2017-06-07T22:06:18.512Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
</pre>
<li>HiveServer2 Status<li>
<pre>
curl -u majimenez:cloudera 'http://ec2-34-251-6-22.eu-west-1.compute.amazonaws.com:7180/api/v12/clusters/majimenez/services/hive'
</pre>
<pre>
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-2-87.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-2-87.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
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
  }, {
    "name" : "HIVE_WEBHCATS_HEALTHY",
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
</pre>
<ul>