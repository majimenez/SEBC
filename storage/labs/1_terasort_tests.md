<b>1. Teragen Results</b>
<pre>
time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.8.3.jar teragen -Ddfs.block.size=33554432 -Dmapred.map.tasks=4 107374182 tera_gen10G
17/06/07 08:47:28 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-201.eu-west-1.compute.internal/172.31.0.201:8032
17/06/07 08:47:29 INFO terasort.TeraSort: Generating 107374182 using 4
17/06/07 08:47:29 INFO mapreduce.JobSubmitter: number of splits:4
17/06/07 08:47:29 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/06/07 08:47:29 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/06/07 08:47:29 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1496798853181_0002
17/06/07 08:47:29 INFO impl.YarnClientImpl: Submitted application application_1496798853181_0002
17/06/07 08:47:29 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-201.eu-west-1.compute.internal:8088/proxy/application_1496798853181_0002/
17/06/07 08:47:29 INFO mapreduce.Job: Running job: job_1496798853181_0002
17/06/07 08:47:36 INFO mapreduce.Job: Job job_1496798853181_0002 running in uber mode : false
17/06/07 08:47:36 INFO mapreduce.Job:  map 0% reduce 0%
17/06/07 08:47:47 INFO mapreduce.Job:  map 3% reduce 0%
17/06/07 08:47:48 INFO mapreduce.Job:  map 10% reduce 0%
[...truncated...]
17/06/07 08:50:01 INFO mapreduce.Job:  map 99% reduce 0%
17/06/07 08:50:03 INFO mapreduce.Job:  map 100% reduce 0%
17/06/07 08:50:03 INFO mapreduce.Job: Job job_1496798853181_0002 completed successfully
17/06/07 08:50:03 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=488444
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=344
		HDFS: Number of bytes written=10737418200
		HDFS: Number of read operations=16
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=8
	Job Counters 
		Launched map tasks=4
		Other local map tasks=4
		Total time spent by all maps in occupied slots (ms)=572475
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=572475
		Total vcore-seconds taken by all map tasks=572475
		Total megabyte-seconds taken by all map tasks=586214400
	Map-Reduce Framework
		Map input records=107374182
		Map output records=107374182
		Input split bytes=344
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=906
		CPU time spent (ms)=169560
		Physical memory (bytes) snapshot=1405550592
		Virtual memory (bytes) snapshot=11134881792
		Total committed heap usage (bytes)=796393472
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=230593859918397906
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=10737418200

real	2m37.496s
user	0m6.955s
sys	0m0.892s

</pre>

<b>2. Terasort results</b>
<pre>

time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.8.3.jar terasort tera_gen10G tera_sort_10G
17/06/07 08:53:09 INFO terasort.TeraSort: starting
17/06/07 08:53:10 INFO input.FileInputFormat: Total input paths to process : 4
Spent 212ms computing base-splits.
Spent 8ms computing TeraScheduler splits.
Computing input splits took 221ms
Sampling 10 splits of 320
Making 6 from 100000 sampled records
Computing parititions took 824ms
Spent 1047ms computing partitions.
17/06/07 08:53:11 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-201.eu-west-1.compute.internal/172.31.0.201:8032
17/06/07 08:53:12 INFO mapreduce.JobSubmitter: number of splits:320
17/06/07 08:53:12 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1496798853181_0003
17/06/07 08:53:12 INFO impl.YarnClientImpl: Submitted application application_1496798853181_0003
17/06/07 08:53:13 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-201.eu-west-1.compute.internal:8088/proxy/application_1496798853181_0003/
17/06/07 08:53:13 INFO mapreduce.Job: Running job: job_1496798853181_0003
17/06/07 08:53:19 INFO mapreduce.Job: Job job_1496798853181_0003 running in uber mode : false
17/06/07 08:53:19 INFO mapreduce.Job:  map 0% reduce 0%
17/06/07 08:53:27 INFO mapreduce.Job:  map 1% reduce 0%
...
17/06/07 09:00:41 INFO mapreduce.Job:  map 100% reduce 99%
17/06/07 09:00:44 INFO mapreduce.Job:  map 100% reduce 100%
17/06/07 09:00:44 INFO mapreduce.Job: Job job_1496798853181_0003 completed successfully
17/06/07 09:00:44 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=4815269703
		FILE: Number of bytes written=9553110508
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=10737469080
		HDFS: Number of bytes written=10737418200
		HDFS: Number of read operations=978
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=12
	Job Counters 
		Launched map tasks=320
		Launched reduce tasks=6
		Data-local map tasks=320
		Total time spent by all maps in occupied slots (ms)=2610343
		Total time spent by all reduces in occupied slots (ms)=822023
		Total time spent by all map tasks (ms)=2610343
		Total time spent by all reduce tasks (ms)=822023
		Total vcore-seconds taken by all map tasks=2610343
		Total vcore-seconds taken by all reduce tasks=822023
		Total megabyte-seconds taken by all map tasks=2672991232
		Total megabyte-seconds taken by all reduce tasks=841751552
	Map-Reduce Framework
		Map input records=107374182
		Map output records=107374182
		Map output bytes=10952166564
		Map output materialized bytes=4697547721
		Input split bytes=50880
		Combine input records=0
		Combine output records=0
		Reduce input groups=107374182
		Reduce shuffle bytes=4697547721
		Reduce input records=107374182
		Reduce output records=107374182
		Spilled Records=214748364
		Shuffled Maps =1920
		Failed Shuffles=0
		Merged Map outputs=1920
		GC time elapsed (ms)=48043
		CPU time spent (ms)=1612480
		Physical memory (bytes) snapshot=152757526528
		Virtual memory (bytes) snapshot=903330897920
		Total committed heap usage (bytes)=159330074624
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters 
		Bytes Read=10737418200
	File Output Format Counters 
		Bytes Written=10737418200
17/06/07 09:00:44 INFO terasort.TeraSort: done

real	7m35.764s
user	0m10.442s
sys	0m1.077s
</pre>