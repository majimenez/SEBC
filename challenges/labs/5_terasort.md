<pre>
time hadoop jar /opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort tgen512m tgenout
</pre>

output
<pre>

</pre>

<pre>
time hadoop jar /opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar PI
</pre>
output
<pre>
time hadoop jar /opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort tgen512m tgenout
17/06/09 10:50:51 INFO terasort.TeraSort: starting
17/06/09 10:50:52 INFO hdfs.DFSClient: Created token for theresa: HDFS_DELEGATION_TOKEN owner=theresa@MAJIMENEZ.CO.UK, renewer=yarn, realUser=, issueDate=1497005453000, maxDate=1497610253000, sequenceNumber=1, masterKeyId=2 on 172.31.33.96:8020
17/06/09 10:50:53 INFO security.TokenCache: Got dt for hdfs://ip-172-31-33-96.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.33.96:8020, Ident: (token for theresa: HDFS_DELEGATION_TOKEN owner=theresa@MAJIMENEZ.CO.UK, renewer=yarn, realUser=, issueDate=1497005453000, maxDate=1497610253000, sequenceNumber=1, masterKeyId=2)
17/06/09 10:50:53 INFO input.FileInputFormat: Total input paths to process : 2
Spent 380ms computing base-splits.
Spent 3ms computing TeraScheduler splits.
Computing input splits took 384ms
Sampling 10 splits of 38
Making 8 from 100000 sampled records
Computing parititions took 824ms
Spent 1210ms computing partitions.
17/06/09 10:50:53 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-33-96.eu-west-1.compute.internal/172.31.33.96:8032
17/06/09 10:50:54 INFO mapreduce.JobSubmitter: number of splits:38
17/06/09 10:50:54 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1497005335817_0001
17/06/09 10:50:54 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.33.96:8020, Ident: (token for theresa: HDFS_DELEGATION_TOKEN owner=theresa@MAJIMENEZ.CO.UK, renewer=yarn, realUser=, issueDate=1497005453000, maxDate=1497610253000, sequenceNumber=1, masterKeyId=2)
17/06/09 10:50:55 INFO impl.YarnClientImpl: Submitted application application_1497005335817_0001
17/06/09 10:50:55 INFO mapreduce.Job: The url to track the job: http://ip-172-31-33-96.eu-west-1.compute.internal:8088/proxy/application_1497005335817_0001/
17/06/09 10:50:55 INFO mapreduce.Job: Running job: job_1497005335817_0001
17/06/09 10:51:06 INFO mapreduce.Job: Job job_1497005335817_0001 running in uber mode : false
17/06/09 10:51:06 INFO mapreduce.Job:  map 0% reduce 0%
17/06/09 10:51:20 INFO mapreduce.Job:  map 3% reduce 0%
17/06/09 10:51:21 INFO mapreduce.Job:  map 11% reduce 0%
17/06/09 10:51:23 INFO mapreduce.Job:  map 13% reduce 0%
17/06/09 10:51:24 INFO mapreduce.Job:  map 16% reduce 0%
17/06/09 10:51:28 INFO mapreduce.Job:  map 18% reduce 0%
17/06/09 10:51:32 INFO mapreduce.Job:  map 29% reduce 0%
17/06/09 10:51:34 INFO mapreduce.Job:  map 34% reduce 0%
17/06/09 10:51:35 INFO mapreduce.Job:  map 42% reduce 0%
17/06/09 10:51:37 INFO mapreduce.Job:  map 45% reduce 0%
17/06/09 10:51:46 INFO mapreduce.Job:  map 53% reduce 0%
17/06/09 10:51:47 INFO mapreduce.Job:  map 58% reduce 0%
17/06/09 10:51:48 INFO mapreduce.Job:  map 61% reduce 0%
17/06/09 10:51:49 INFO mapreduce.Job:  map 66% reduce 0%
17/06/09 10:51:50 INFO mapreduce.Job:  map 71% reduce 0%
17/06/09 10:51:55 INFO mapreduce.Job:  map 74% reduce 0%
17/06/09 10:51:57 INFO mapreduce.Job:  map 79% reduce 0%
17/06/09 10:52:01 INFO mapreduce.Job:  map 84% reduce 0%
17/06/09 10:52:02 INFO mapreduce.Job:  map 87% reduce 0%
17/06/09 10:52:04 INFO mapreduce.Job:  map 89% reduce 0%
17/06/09 10:52:06 INFO mapreduce.Job:  map 92% reduce 0%
17/06/09 10:52:07 INFO mapreduce.Job:  map 100% reduce 0%
17/06/09 10:52:19 INFO mapreduce.Job:  map 100% reduce 19%
17/06/09 10:52:20 INFO mapreduce.Job:  map 100% reduce 29%
17/06/09 10:52:21 INFO mapreduce.Job:  map 100% reduce 46%
17/06/09 10:52:23 INFO mapreduce.Job:  map 100% reduce 54%
17/06/09 10:52:24 INFO mapreduce.Job:  map 100% reduce 64%
17/06/09 10:52:25 INFO mapreduce.Job:  map 100% reduce 78%
17/06/09 10:52:26 INFO mapreduce.Job:  map 100% reduce 80%
17/06/09 10:52:27 INFO mapreduce.Job:  map 100% reduce 83%
17/06/09 10:52:28 INFO mapreduce.Job:  map 100% reduce 84%
17/06/09 10:52:29 INFO mapreduce.Job:  map 100% reduce 86%
17/06/09 10:52:30 INFO mapreduce.Job:  map 100% reduce 88%
17/06/09 10:52:31 INFO mapreduce.Job:  map 100% reduce 90%
17/06/09 10:52:33 INFO mapreduce.Job:  map 100% reduce 96%
17/06/09 10:52:34 INFO mapreduce.Job:  map 100% reduce 97%
17/06/09 10:52:35 INFO mapreduce.Job:  map 100% reduce 100%
17/06/09 10:52:36 INFO mapreduce.Job: Job job_1497005335817_0001 completed successfully
17/06/09 10:52:36 INFO mapreduce.Job: Counters: 50
	File System Counters
		FILE: Number of bytes read=2292563865
		FILE: Number of bytes written=4553558021
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=5120005852
		HDFS: Number of bytes written=5120000000
		HDFS: Number of read operations=138
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=16
	Job Counters 
		Launched map tasks=38
		Launched reduce tasks=8
		Data-local map tasks=37
		Rack-local map tasks=1
		Total time spent by all maps in occupied slots (ms)=520606
		Total time spent by all reduces in occupied slots (ms)=213438
		Total time spent by all map tasks (ms)=520606
		Total time spent by all reduce tasks (ms)=213438
		Total vcore-seconds taken by all map tasks=520606
		Total vcore-seconds taken by all reduce tasks=213438
		Total megabyte-seconds taken by all map tasks=533100544
		Total megabyte-seconds taken by all reduce tasks=218560512
	Map-Reduce Framework
		Map input records=51200000
		Map output records=51200000
		Map output bytes=5222400000
		Map output materialized bytes=2255152514
		Input split bytes=5852
		Combine input records=0
		Combine output records=0
		Reduce input groups=51200000
		Reduce shuffle bytes=2255152514
		Reduce input records=51200000
		Reduce output records=51200000
		Spilled Records=102400000
		Shuffled Maps =304
		Failed Shuffles=0
		Merged Map outputs=304
		GC time elapsed (ms)=13085
		CPU time spent (ms)=510150
		Physical memory (bytes) snapshot=27097788416
		Virtual memory (bytes) snapshot=128099180544
		Total committed heap usage (bytes)=27184332800
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters 
		Bytes Read=5120000000
	File Output Format Counters 
		Bytes Written=5120000000
17/06/09 10:52:36 INFO terasort.TeraSort: done

real	1m46.713s
user	0m9.838s
sys	0m1.038s
</pre>