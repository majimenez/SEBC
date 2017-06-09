hdfs dfs -ls /user
<pre>
hadoop fs -ls /user
Found 6 items
drwxrwxrwx   - mapred  hadoop              0 2017-06-09 09:57 /user/history
drwxrwxr-t   - hive    hive                0 2017-06-09 09:57 /user/hive
drwxrwxr-x   - hue     hue                 0 2017-06-09 09:58 /user/hue
drwxr-xr-x   - jeremy  supergroup          0 2017-06-09 10:06 /user/jeremy
drwxrwxr-x   - oozie   oozie               0 2017-06-09 09:58 /user/oozie
drwxr-xr-x   - theresa supergroup          0 2017-06-09 10:06 /user/theresa
</pre>

<br/>
curl -u admin:admin http://ip-172-31-41-42:7180/api/v14/hosts
<pre>
{
  "items" : [ {
    "hostId" : "bce9e6dc-39c1-4ab0-83b4-90d4cd242e1b",
    "ipAddress" : "172.31.32.90",
    "hostname" : "ip-172-31-32-90.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-41-42.eu-west-1.compute.internal:7180/cmf/hostRedirect/bce9e6dc-39c1-4ab0-83b4-90d4cd242e1b",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "cb424413-ab29-4a60-b6fd-075ef02611d6",
    "ipAddress" : "172.31.33.96",
    "hostname" : "ip-172-31-33-96.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-41-42.eu-west-1.compute.internal:7180/cmf/hostRedirect/cb424413-ab29-4a60-b6fd-075ef02611d6",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "5b879fef-af19-40c5-a368-8ed949c8d9d0",
    "ipAddress" : "172.31.37.252",
    "hostname" : "ip-172-31-37-252.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-41-42.eu-west-1.compute.internal:7180/cmf/hostRedirect/5b879fef-af19-40c5-a368-8ed949c8d9d0",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "b65b8213-2d93-4f3c-8508-34036123a6c8",
    "ipAddress" : "172.31.39.2",
    "hostname" : "ip-172-31-39-2.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-41-42.eu-west-1.compute.internal:7180/cmf/hostRedirect/b65b8213-2d93-4f3c-8508-34036123a6c8",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "3a88208d-6695-4a68-8ba3-869d16ffd702",
    "ipAddress" : "172.31.41.42",
    "hostname" : "ip-172-31-41-42.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-41-42.eu-west-1.compute.internal:7180/cmf/hostRedirect/3a88208d-6695-4a68-8ba3-869d16ffd702",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  } ]
  </pre>
