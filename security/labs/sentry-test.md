<h1>Verify user privileges</h1>
<li>Authenticate your user as a Kerberos principal</li>
<pre>
[root@ip-172-31-2-87 ~]# kinit majimenez
Password for majimenez@MAJIMENEZ.ES: 
</pre>
<li>Use beeline to confirm your principal sees no tables
<pre>beeline
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> 
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-2-87.eu-west-1.compute.internal@MAJIMENEZ.ES
scan complete in 3ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-2-87.eu-west-1.compute.internal@MAJIMENEZ.ES
Enter username for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-2-87.eu-west-1.compute.internal@MAJIMENEZ.ES: majimenez
Enter password for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-2-87.eu-west-1.compute.internal@MAJIMENEZ.ES: *********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default>
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170608092121_4b1e6eb0-429c-4466-8b91-b597a5d78e2b): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170608092121_4b1e6eb0-429c-4466-8b91-b597a5d78e2b); Time taken: 0.105 seconds
INFO  : Executing command(queryId=hive_20170608092121_4b1e6eb0-429c-4466-8b91-b597a5d78e2b): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608092121_4b1e6eb0-429c-4466-8b91-b597a5d78e2b); Time taken: 0.157 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (0.417 seconds)
</pre>

<h1>kinit as george, then login to beeline</h1>

<b>george should be able to see all tables</b>
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170608092525_4c8b1eea-8700-4b3f-8c8f-6069f67d64eb): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170608092525_4c8b1eea-8700-4b3f-8c8f-6069f67d64eb); Time taken: 0.073 seconds
INFO  : Executing command(queryId=hive_20170608092525_4c8b1eea-8700-4b3f-8c8f-6069f67d64eb): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608092525_4c8b1eea-8700-4b3f-8c8f-6069f67d64eb); Time taken: 0.132 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.337 seconds)

<b>ferdinand should see sample_07</b>
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170608092828_ebe4d062-3c65-49c5-be2d-05d1f4d0f5c9): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170608092828_ebe4d062-3c65-49c5-be2d-05d1f4d0f5c9); Time taken: 0.077 seconds
INFO  : Executing command(queryId=hive_20170608092828_ebe4d062-3c65-49c5-be2d-05d1f4d0f5c9): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608092828_ebe4d062-3c65-49c5-be2d-05d1f4d0f5c9); Time taken: 0.131 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.354 seconds)
