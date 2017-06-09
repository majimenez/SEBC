<pre>
hadoop jar /opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 2 4
</pre>
<pre>
Number of Maps  = 2
Samples per Map = 4
Wrote input for Map #0
Wrote input for Map #1
Starting Job
17/06/09 10:56:11 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-33-96.eu-west-1.compute.internal/172.31.33.96:8032
17/06/09 10:56:11 INFO hdfs.DFSClient: Created token for jeremy: HDFS_DELEGATION_TOKEN owner=jeremy@MAJIMENEZ.CO.UK, renewer=yarn, realUser=, issueDate=1497005771630, maxDate=1497610571630, sequenceNumber=2, masterKeyId=2 on 172.31.33.96:8020
17/06/09 10:56:11 INFO security.TokenCache: Got dt for hdfs://ip-172-31-33-96.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.33.96:8020, Ident: (token for jeremy: HDFS_DELEGATION_TOKEN owner=jeremy@MAJIMENEZ.CO.UK, renewer=yarn, realUser=, issueDate=1497005771630, maxDate=1497610571630, sequenceNumber=2, masterKeyId=2)
17/06/09 10:56:11 INFO input.FileInputFormat: Total input paths to process : 2
17/06/09 10:56:11 INFO mapreduce.JobSubmitter: number of splits:2
17/06/09 10:56:11 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1497005335817_0002
17/06/09 10:56:11 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.33.96:8020, Ident: (token for jeremy: HDFS_DELEGATION_TOKEN owner=jeremy@MAJIMENEZ.CO.UK, renewer=yarn, realUser=, issueDate=1497005771630, maxDate=1497610571630, sequenceNumber=2, masterKeyId=2)
17/06/09 10:56:12 INFO impl.YarnClientImpl: Submitted application application_1497005335817_0002
17/06/09 10:56:12 INFO mapreduce.Job: The url to track the job: http://ip-172-31-33-96.eu-west-1.compute.internal:8088/proxy/application_1497005335817_0002/
17/06/09 10:56:12 INFO mapreduce.Job: Running job: job_1497005335817_0002
17/06/09 10:56:21 INFO mapreduce.Job: Job job_1497005335817_0002 running in uber mode : false
17/06/09 10:56:21 INFO mapreduce.Job:  map 0% reduce 0%
17/06/09 10:56:26 INFO mapreduce.Job:  map 50% reduce 0%
17/06/09 10:56:29 INFO mapreduce.Job:  map 100% reduce 0%
17/06/09 10:56:35 INFO mapreduce.Job:  map 100% reduce 100%
17/06/09 10:56:36 INFO mapreduce.Job: Job job_1497005335817_0002 completed successfully
17/06/09 10:56:36 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=47
		FILE: Number of bytes written=378674
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=596
		HDFS: Number of bytes written=215
		HDFS: Number of read operations=11
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=3
	Job Counters 
		Launched map tasks=2
		Launched reduce tasks=1
		Data-local map tasks=2
		Total time spent by all maps in occupied slots (ms)=9321
		Total time spent by all reduces in occupied slots (ms)=3494
		Total time spent by all map tasks (ms)=9321
		Total time spent by all reduce tasks (ms)=3494
		Total vcore-seconds taken by all map tasks=9321
		Total vcore-seconds taken by all reduce tasks=3494
		Total megabyte-seconds taken by all map tasks=9544704
		Total megabyte-seconds taken by all reduce tasks=3577856
	Map-Reduce Framework
		Map input records=2
		Map output records=4
		Map output bytes=36
		Map output materialized bytes=67
		Input split bytes=360
		Combine input records=0
		Combine output records=0
		Reduce input groups=2
		Reduce shuffle bytes=67
		Reduce input records=4
		Reduce output records=0
		Spilled Records=8
		Shuffled Maps =2
		Failed Shuffles=0
		Merged Map outputs=2
		GC time elapsed (ms)=169
		CPU time spent (ms)=2690
		Physical memory (bytes) snapshot=1136242688
		Virtual memory (bytes) snapshot=8345833472
		Total committed heap usage (bytes)=1194328064
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters 
		Bytes Read=236
	File Output Format Counters 
		Bytes Written=97
Job Finished in 25.61 seconds
Estimated value of Pi is 3.50000000000000000000

real	0m28.831s
user	0m9.125s
sys	0m1.103s
</pre>