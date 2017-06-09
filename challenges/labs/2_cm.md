<h1>List the command and output of ls /etc/yum.repos.d in challenges/labs/2_cm.md</h1>
<pre>
ls /etc/yum.repos.d
CentOS-Base.repo  CentOS-Debuginfo.repo  CentOS-Media.repo  CentOS-Vault.repo  cloudera-manager.repo  mysql-community.repo  mysql-community-source.repo
</pre>

<h1>Use the scm_prepare_database.sh script to write your db.properties file</h1>
<pre>
/usr/share/cmf/schema/scm_prepare_database.sh mysql cloudera cloudera T3mp0r@l -h ip-172-31-37-252 
JAVA_HOME=/usr/java/jdk1.8.0_91
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.8.0_91/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!
</pre>
