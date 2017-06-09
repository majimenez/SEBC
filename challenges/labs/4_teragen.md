<pre>
time hadoop jar /opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen  -Ddsf.block.size=32M 51200000 tgen512m
</pre>

<pre>
17/06/09 10:18:50 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-33-96.eu-west-1.compute.internal/172.31.33.96:8032
17/06/09 10:18:51 INFO terasort.TeraGen: Generating 51200000 using 2
17/06/09 10:18:51 INFO mapreduce.JobSubmitter: number of splits:2
17/06/09 10:18:51 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1497002707732_0001
17/06/09 10:18:52 INFO impl.YarnClientImpl: Submitted application application_1497002707732_0001
17/06/09 10:18:52 INFO mapreduce.Job: The url to track the job: http://ip-172-31-33-96.eu-west-1.compute.internal:8088/proxy/application_1497002707732_0001/
17/06/09 10:18:52 INFO mapreduce.Job: Running job: job_1497002707732_0001
17/06/09 10:19:00 INFO mapreduce.Job: Job job_1497002707732_0001 running in uber mode : false
17/06/09 10:19:00 INFO mapreduce.Job:  map 0% reduce 0%
17/06/09 10:19:19 INFO mapreduce.Job:  map 25% reduce 0%
17/06/09 10:19:25 INFO mapreduce.Job:  map 32% reduce 0%
17/06/09 10:19:31 INFO mapreduce.Job:  map 39% reduce 0%
17/06/09 10:19:38 INFO mapreduce.Job:  map 46% reduce 0%
17/06/09 10:19:44 INFO mapreduce.Job:  map 53% reduce 0%
17/06/09 10:19:50 INFO mapreduce.Job:  map 60% reduce 0%
17/06/09 10:19:56 INFO mapreduce.Job:  map 66% reduce 0%
17/06/09 10:20:02 INFO mapreduce.Job:  map 75% reduce 0%
17/06/09 10:20:07 INFO mapreduce.Job:  map 78% reduce 0%
17/06/09 10:20:08 INFO mapreduce.Job:  map 82% reduce 0%
17/06/09 10:20:14 INFO mapreduce.Job:  map 85% reduce 0%
17/06/09 10:20:15 INFO mapreduce.Job:  map 89% reduce 0%
17/06/09 10:20:20 INFO mapreduce.Job:  map 95% reduce 0%
17/06/09 10:20:24 INFO mapreduce.Job:  map 100% reduce 0%
17/06/09 10:20:24 INFO mapreduce.Job: Job job_1497002707732_0001 completed successfully
17/06/09 10:20:24 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=249750
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=170
		HDFS: Number of bytes written=5120000000
		HDFS: Number of read operations=8
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=4
	Job Counters 
		Launched map tasks=2
		Other local map tasks=2
		Total time spent by all maps in occupied slots (ms)=162040
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=162040
		Total vcore-seconds taken by all map tasks=162040
		Total megabyte-seconds taken by all map tasks=165928960
	Map-Reduce Framework
		Map input records=51200000
		Map output records=51200000
		Input split bytes=170
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=405
		CPU time spent (ms)=79870
		Physical memory (bytes) snapshot=741883904
		Virtual memory (bytes) snapshot=5563998208
		Total committed heap usage (bytes)=601882624
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=109963291816450258
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=5120000000
</pre>
<pre>
real	1m36.109s
user	0m7.980s
sys	0m0.999s
</pre>
<pre>
hdfs dfs -ls /user/theresa/tgen512m
Found 3 items
-rw-r--r--   3 theresa supergroup          0 2017-06-09 10:20 /user/theresa/tgen512m/_SUCCESS
-rw-r--r--   3 theresa supergroup 2560000000 2017-06-09 10:20 /user/theresa/tgen512m/part-m-00000
-rw-r--r--   3 theresa supergroup 2560000000 2017-06-09 10:20 /user/theresa/tgen512m/part-m-00001
</pre>
<pre>
<pre>
hdfs fsck /user/theresa/tgen512m/ -blocks -files
Connecting to namenode via http://ip-172-31-33-96.eu-west-1.compute.internal:50070
FSCK started by theresa (auth:SIMPLE) from /172.31.41.42 for path /user/theresa/tgen512m/ at Fri Jun 09 10:23:32 UTC 2017
/user/theresa/tgen512m/ <dir>
/user/theresa/tgen512m/_SUCCESS 0 bytes, 0 block(s):  OK

/user/theresa/tgen512m/part-m-00000 2560000000 bytes, 20 block(s):  OK
0. BP-1921893275-172.31.33.96-1497002176011:blk_1073742509_1685 len=134217728 Live_repl=3
1. BP-1921893275-172.31.33.96-1497002176011:blk_1073742510_1686 len=134217728 Live_repl=3
2. BP-1921893275-172.31.33.96-1497002176011:blk_1073742512_1688 len=134217728 Live_repl=3
3. BP-1921893275-172.31.33.96-1497002176011:blk_1073742514_1690 len=134217728 Live_repl=3
4. BP-1921893275-172.31.33.96-1497002176011:blk_1073742516_1692 len=134217728 Live_repl=3
5. BP-1921893275-172.31.33.96-1497002176011:blk_1073742518_1694 len=134217728 Live_repl=3
6. BP-1921893275-172.31.33.96-1497002176011:blk_1073742520_1696 len=134217728 Live_repl=3
7. BP-1921893275-172.31.33.96-1497002176011:blk_1073742522_1698 len=134217728 Live_repl=3
8. BP-1921893275-172.31.33.96-1497002176011:blk_1073742524_1700 len=134217728 Live_repl=3
9. BP-1921893275-172.31.33.96-1497002176011:blk_1073742527_1703 len=134217728 Live_repl=3
10. BP-1921893275-172.31.33.96-1497002176011:blk_1073742529_1705 len=134217728 Live_repl=3
11. BP-1921893275-172.31.33.96-1497002176011:blk_1073742531_1707 len=134217728 Live_repl=3
12. BP-1921893275-172.31.33.96-1497002176011:blk_1073742534_1710 len=134217728 Live_repl=3
13. BP-1921893275-172.31.33.96-1497002176011:blk_1073742536_1712 len=134217728 Live_repl=3
14. BP-1921893275-172.31.33.96-1497002176011:blk_1073742537_1713 len=134217728 Live_repl=3
15. BP-1921893275-172.31.33.96-1497002176011:blk_1073742539_1715 len=134217728 Live_repl=3
16. BP-1921893275-172.31.33.96-1497002176011:blk_1073742541_1717 len=134217728 Live_repl=3
17. BP-1921893275-172.31.33.96-1497002176011:blk_1073742543_1719 len=134217728 Live_repl=3
18. BP-1921893275-172.31.33.96-1497002176011:blk_1073742545_1721 len=134217728 Live_repl=3
19. BP-1921893275-172.31.33.96-1497002176011:blk_1073742547_1723 len=9863168 Live_repl=3

/user/theresa/tgen512m/part-m-00001 2560000000 bytes, 20 block(s):  OK
0. BP-1921893275-172.31.33.96-1497002176011:blk_1073742508_1684 len=134217728 Live_repl=3
1. BP-1921893275-172.31.33.96-1497002176011:blk_1073742511_1687 len=134217728 Live_repl=3
2. BP-1921893275-172.31.33.96-1497002176011:blk_1073742513_1689 len=134217728 Live_repl=3
3. BP-1921893275-172.31.33.96-1497002176011:blk_1073742515_1691 len=134217728 Live_repl=3
4. BP-1921893275-172.31.33.96-1497002176011:blk_1073742517_1693 len=134217728 Live_repl=3
5. BP-1921893275-172.31.33.96-1497002176011:blk_1073742519_1695 len=134217728 Live_repl=3
6. BP-1921893275-172.31.33.96-1497002176011:blk_1073742521_1697 len=134217728 Live_repl=3
7. BP-1921893275-172.31.33.96-1497002176011:blk_1073742523_1699 len=134217728 Live_repl=3
8. BP-1921893275-172.31.33.96-1497002176011:blk_1073742525_1701 len=134217728 Live_repl=3
9. BP-1921893275-172.31.33.96-1497002176011:blk_1073742528_1704 len=134217728 Live_repl=3
10. BP-1921893275-172.31.33.96-1497002176011:blk_1073742530_1706 len=134217728 Live_repl=3
11. BP-1921893275-172.31.33.96-1497002176011:blk_1073742532_1708 len=134217728 Live_repl=3
12. BP-1921893275-172.31.33.96-1497002176011:blk_1073742533_1709 len=134217728 Live_repl=3
13. BP-1921893275-172.31.33.96-1497002176011:blk_1073742535_1711 len=134217728 Live_repl=3
14. BP-1921893275-172.31.33.96-1497002176011:blk_1073742538_1714 len=134217728 Live_repl=3
15. BP-1921893275-172.31.33.96-1497002176011:blk_1073742540_1716 len=134217728 Live_repl=3
16. BP-1921893275-172.31.33.96-1497002176011:blk_1073742542_1718 len=134217728 Live_repl=3
17. BP-1921893275-172.31.33.96-1497002176011:blk_1073742544_1720 len=134217728 Live_repl=3
18. BP-1921893275-172.31.33.96-1497002176011:blk_1073742546_1722 len=134217728 Live_repl=3
19. BP-1921893275-172.31.33.96-1497002176011:blk_1073742548_1724 len=9863168 Live_repl=3

Status: HEALTHY
 Total size:	5120000000 B
 Total dirs:	1
 Total files:	3
 Total symlinks:		0
 Total blocks (validated):	40 (avg. block size 128000000 B)
 Minimally replicated blocks:	40 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		4
 Number of racks:		1
FSCK ended at Fri Jun 09 10:23:32 UTC 2017 in 3 milliseconds


The filesystem under path '/user/theresa/tgen512m/' is HEALTHY
</pre>
</pre>