<b>Report the latest available version of the API</b>
<pre>
curl -u majimenez:cloudera http://ec2-34-251-6-22.eu-west-1.compute.amazonaws.com:7180/api/version
v14
</pre>
<b>Report the CM version</b>
<pre>
curl -u majimenez:cloudera http://ec2-34-251-6-22.eu-west-1.compute.amazonaws.com:7180/api/v14/cm/version
{
  "version" : "5.9.2",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170330-1814",
  "gitHash" : "822da28bff818f57fc1bfc3eafe3a550300ef1b0",
  "snapshot" : false
}
</pre>
<b>List all CM users</b>
<pre>
curl -u majimenez:cloudera http://ec2-34-251-6-22.eu-west-1.compute.amazonaws.com:7180/api/v14/users
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "majimenez",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}
</pre>
<b>Report the database server in use by CM</b>
<pre>
curl -u majimenez:cloudera http://ec2-34-251-6-22.eu-west-1.compute.amazonaws.com:7180/api/v14/cm/scmDbInfo
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
</pre>
