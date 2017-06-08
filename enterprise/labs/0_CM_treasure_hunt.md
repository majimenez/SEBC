<h1>CM Monitoring Lab</h1>
<b>What is ubertask optimization?</b><br/>
Ubertask or small-jobs is a optimization for YARN in which job with few map or reduce (or bytes maximun) tasks will be executed in one only node.

Config Param:<i>mapreduce.job.ubertask.enable</i>=enabled<br/>

Config "Small Job": mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, mapreduce.job.ubertask.maxbytes.<br/>

<i>Docs: https://archive.cloudera.com/cdh5/cdh/5/hadoop/hadoop-mapreduce-client/hadoop-mapreduce-client-core/mapred-default.xml</i><br/>

<b>Where in CM is the Kerberos Security Realm value displayed?</b><br/>
In CM / Search Bar: type "Kerberos Security Realm" / click "conf: security realm" / Find -> Kerberos Security Realm (prop:default_realm, by default: HADOOP.COM)

<b>Which CDH service(s) host a property for enabling Kerberos authentication?</b><br/>
<i>Note: Services which aren't installed not included</i>
<ul>
<li>HDFS (Web Consoles with SPNEGO)</li>
<li>YARN (Web Consoles with SPNEGO)</li>
<li>ZOOKEEPER</li>
</ul>


<b>How do you upgrade the CM agents?</b><br/>

<ol>
<li>Stop Agent: systemctl stop cloudera-scm-agent</li>
<li>Upgrade packets: yum upgrade cloudera-manager-agent</li>
<li>Start Agent: systemctl start cloudera-scm-agent</li>
</ol>

Or through the CM upgrade wizard

<b>Give the tsquery statement used to chart Hue's CPU utilization?</b><br/>

<pre>
select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=HUE
</pre>

<b>Name all the roles that make up the Hive service</b><br/>
<ul>
<li>Hive Metastore Server</li>
<li>Hive Server2</li>
<li>Hive Gateway</li>
<li>WebHCat</li>
</ul>

<b>What steps must be completed before integrating Cloudera Manager with Kerberos?</b><br/>
<ol>
<li>Configuration of DNS and Reverse DNS Resolutions<li>
<li>Install or upgrade the Java JCE Polices</li>
<li>Install krb5-workstation and auth-libs in all nodes</li>
<li>Install krb5-server in the KDC node</li> 
<li>Setup the kdc.conf file and kadmin.acl in the KDC node, specifying the type of encryption for tickets</li>
<li>Create KDC</li>
<li>Continue with Cloudera Manager kerberos wizard</li>
</ol>
