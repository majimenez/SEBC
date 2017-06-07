<b>1. Create a precious directory in HDFS; copy the ZIP course file into it.</b>
<pre>
hdfs dfs -mkdir /user/majimenez/precious
hdfs dfs -put SEBC-master.zip /user/majimenez/precious
</pre>
<b>2. Enable snapshots for precious</b>
Done through Cloudera Manager / Browser / Enable Snapshot<br/>
<b>3. Create a snapshot called sebc-hdfs-test</b>
Done through Cloudera Manager / Browser / Enable Snapshot<br/>
<b>4. Delete the directory</b>
<pre>
hadoop fs -rm -r precious
rm: Failed to move to trash: hdfs://ip-172-31-0-201.eu-west-1.compute.internal:8020/user/majimenez/precious: The directory /user/majimenez/precious cannot be deleted since /user/majimenez/precious is snapshottable and already has snapshots
</pre>
<b>5. Delete the ZIP file</b>
<pre>
hadoop fs -rm -r precious/SEBC-master.zip
17/06/07 09:43:53 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-0-201.eu-west-1.compute.internal:8020/user/majimenez/precious/SEBC-master.zip' to trash at: hdfs://ip-172-31-0-201.eu-west-1.compute.internal:8020/user/majimenez/.Trash/Current/user/majimenez/precious/SEBC-master.zip1496828633483
hadoop fs -ls precious
>
</pre>
<b>6. Restore the deleted file</b>
Done through Cloudera Manager / Browser / Restore Directory From Snapshot<br/>
<pre>
hadoop fs -ls precious
Found 1 items
-rw-r--r--   3 hdfs supergroup     818460 2017-06-07 09:45 precious/SEBC-master.zip
</pre>
