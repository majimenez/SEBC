
<b>1. Name a source directory after your GitHub handle</b>
<pre>
As root:
hdfs dfs -ls /user/majimenez
</pre>
<b>Name a target directory after your partner's GitHub handle</b>
<pre>
hdfs dfs -mkdir /user/ainowy/
hdfs dfs -chown -R ainowy
</pre>

<b>3. Use teragen to create a 500 MB file</b>
<pre>
hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.8.3.jar teragen 5242880 tera_gen
17/06/07 08:35:20 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-201.eu-west-1.compute.internal/172.31.0.201:8032
17/06/07 08:35:21 INFO terasort.TeraSort: Generating 5242880 using 2
17/06/07 08:35:21 INFO mapreduce.JobSubmitter: number of splits:2
17/06/07 08:35:21 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1496798853181_0001
17/06/07 08:35:22 INFO impl.YarnClientImpl: Submitted application application_1496798853181_0001
17/06/07 08:35:22 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-201.eu-west-1.compute.internal:8088/proxy/application_1496798853181_0001/
17/06/07 08:35:22 INFO mapreduce.Job: Running job: job_1496798853181_0001
17/06/07 08:35:29 INFO mapreduce.Job: Job job_1496798853181_0001 running in uber mode : false
17/06/07 08:35:29 INFO mapreduce.Job:  map 0% reduce 0%
17/06/07 08:35:39 INFO mapreduce.Job:  map 50% reduce 0%
17/06/07 08:35:40 INFO mapreduce.Job:  map 100% reduce 0%
17/06/07 08:35:40 INFO mapreduce.Job: Job job_1496798853181_0001 completed successfully
17/06/07 08:35:40 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=244214
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=167
		HDFS: Number of bytes written=524288000
		HDFS: Number of read operations=8
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=4
	Job Counters 
		Launched map tasks=2
		Other local map tasks=2
		Total time spent by all maps in occupied slots (ms)=15766
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=15766
		Total vcore-seconds taken by all map tasks=15766
		Total megabyte-seconds taken by all map tasks=16144384
	Map-Reduce Framework
		Map input records=5242880
		Map output records=5242880
		Input split bytes=167
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=159
		CPU time spent (ms)=14840
		Physical memory (bytes) snapshot=612806656
		Virtual memory (bytes) snapshot=5538983936
		Total committed heap usage (bytes)=682098688
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=11257830824958050
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=524288000
[root@ip-172-31-0-201 ~]# hadoop fs -ls tera_gen
Found 3 items
-rw-r--r--   3 majimenez supergroup          0 2017-06-07 08:35 tera_gen/_SUCCESS
-rw-r--r--   3 majimenez supergroup  262144000 2017-06-07 08:35 tera_gen/part-m-00000
-rw-r--r--   3 majimenez supergroup  262144000 2017-06-07 08:35 tera_gen/part-m-00001
</pre>
<b>3. Copy your partner's file to your target directory</b>
	<ul>
		<li>Let one partner use distCp on the command line</li>
		<pre>
		hadoop distcp hdfs:///user/majimenez/tera_gen hdfs://34.250.247.218:8020/user/majimenez
		</pre>
		<pre>
17/06/07 10:53:03 INFO tools.DistCp: Input Options: DistCpOptions{atomicCommit=false, syncFolder=false, deleteMissing=false, ignoreFailures=false, overwrite=false, skipCRC=false, blocking=true, numListstatusThreads=0, maxMaps=20, mapBandwidth=100, sslConfigurationFile='null', copyStrategy='uniformsize', preserveStatus=[], preserveRawXattrs=false, atomicWorkPath=null, logPath=null, sourceFileListing=null, sourcePaths=[hdfs:/user/majimenez/tera_gen], targetPath=hdfs://34.250.247.218:8020/user/majimenez, targetPathExists=true, filtersFile='null'}
17/06/07 10:53:03 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-201.eu-west-1.compute.internal/172.31.0.201:8032
17/06/07 10:53:03 INFO tools.SimpleCopyListing: Paths (files+dirs) cnt = 4; dirCnt = 1
17/06/07 10:53:03 INFO tools.SimpleCopyListing: Build file listing completed.
17/06/07 10:53:03 INFO Configuration.deprecation: io.sort.mb is deprecated. Instead, use mapreduce.task.io.sort.mb
17/06/07 10:53:03 INFO Configuration.deprecation: io.sort.factor is deprecated. Instead, use mapreduce.task.io.sort.factor
17/06/07 10:53:03 INFO tools.DistCp: Number of paths in the copy list: 4
17/06/07 10:53:04 INFO tools.DistCp: Number of paths in the copy list: 4
17/06/07 10:53:04 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-201.eu-west-1.compute.internal/172.31.0.201:8032
17/06/07 10:53:04 INFO mapreduce.JobSubmitter: number of splits:3
17/06/07 10:53:04 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1496798853181_0006
17/06/07 10:53:04 INFO impl.YarnClientImpl: Submitted application application_1496798853181_0006
17/06/07 10:53:04 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-201.eu-west-1.compute.internal:8088/proxy/application_1496798853181_0006/
17/06/07 10:53:04 INFO tools.DistCp: DistCp job-id: job_1496798853181_0006
17/06/07 10:53:04 INFO mapreduce.Job: Running job: job_1496798853181_0006
17/06/07 10:53:11 INFO mapreduce.Job: Job job_1496798853181_0006 running in uber mode : false
17/06/07 10:53:11 INFO mapreduce.Job:  map 0% reduce 0%
17/06/07 10:53:16 INFO mapreduce.Job:  map 33% reduce 0%
17/06/07 10:53:21 INFO mapreduce.Job:  map 100% reduce 0% 
</pre>
</ul>

<b>Use hdfs fsck < path > -files -blocks on your source and target directories</b>
<pre>
root@ip-172-31-0-201 ~]# hdfs fsck /user/majimenez/tera_gen -files -blocks
Connecting to namenode via http://ip-172-31-0-201.eu-west-1.compute.internal:50070
FSCK started by root (auth:SIMPLE) from /172.31.0.201 for path /user/majimenez/tera_gen at Wed Jun 07 12:08:02 UTC 2017
/user/majimenez/tera_gen <dir>
/user/majimenez/tera_gen/_SUCCESS 0 bytes, 0 block(s):  OK

/user/majimenez/tera_gen/part-m-00000 262144000 bytes, 2 block(s):  OK
0. BP-79347460-172.31.0.201-1496798794708:blk_1073742951_2127 len=134217728 Live_repl=3
1. BP-79347460-172.31.0.201-1496798794708:blk_1073742953_2129 len=127926272 Live_repl=3

/user/majimenez/tera_gen/part-m-00001 262144000 bytes, 2 block(s):  OK
0. BP-79347460-172.31.0.201-1496798794708:blk_1073742950_2126 len=134217728 Live_repl=3
1. BP-79347460-172.31.0.201-1496798794708:blk_1073742952_2128 len=127926272 Live_repl=3

Status: HEALTHY
 Total size:	524288000 B
 Total dirs:	1
 Total files:	3
 Total symlinks:		0
 Total blocks (validated):	4 (avg. block size 131072000 B)
 Minimally replicated blocks:	4 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		3
 Number of racks:		1
FSCK ended at Wed Jun 07 12:08:02 UTC 2017 in 1 milliseconds


The filesystem under path '/user/majimenez/tera_gen' is HEALTHY
</pre>