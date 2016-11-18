teragen
```
[bavaria@ip-172-31-30-5 tmp]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -D mapred.map.tasks=8 -D dfs.blocksize=16777216 51200000 /user/bavaria/tgen512m
16/11/18 06:06:04 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-17-8.eu-central-1.compute.internal/172.31.17.8:8032
16/11/18 06:06:05 INFO terasort.TeraSort: Generating 51200000 using 8
16/11/18 06:06:05 INFO mapreduce.JobSubmitter: number of splits:8
16/11/18 06:06:05 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
16/11/18 06:06:05 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1479465422055_0005
16/11/18 06:06:05 INFO impl.YarnClientImpl: Submitted application application_1479465422055_0005
16/11/18 06:06:05 INFO mapreduce.Job: The url to track the job: http://ip-172-31-17-8.eu-central-1.compute.internal:8088/proxy/application_1479465422055_0005/
16/11/18 06:06:05 INFO mapreduce.Job: Running job: job_1479465422055_0005
16/11/18 06:06:11 INFO mapreduce.Job: Job job_1479465422055_0005 running in uber mode : false
16/11/18 06:06:11 INFO mapreduce.Job:  map 0% reduce 0%
16/11/18 06:06:22 INFO mapreduce.Job:  map 2% reduce 0%
16/11/18 06:06:23 INFO mapreduce.Job:  map 8% reduce 0%
16/11/18 06:06:24 INFO mapreduce.Job:  map 12% reduce 0%
16/11/18 06:06:25 INFO mapreduce.Job:  map 16% reduce 0%
16/11/18 06:06:26 INFO mapreduce.Job:  map 20% reduce 0%
16/11/18 06:06:27 INFO mapreduce.Job:  map 22% reduce 0%
16/11/18 06:06:28 INFO mapreduce.Job:  map 26% reduce 0%
16/11/18 06:06:29 INFO mapreduce.Job:  map 27% reduce 0%
16/11/18 06:06:30 INFO mapreduce.Job:  map 29% reduce 0%
16/11/18 06:06:31 INFO mapreduce.Job:  map 31% reduce 0%
16/11/18 06:06:32 INFO mapreduce.Job:  map 32% reduce 0%
16/11/18 06:06:33 INFO mapreduce.Job:  map 33% reduce 0%
16/11/18 06:06:34 INFO mapreduce.Job:  map 35% reduce 0%
16/11/18 06:06:35 INFO mapreduce.Job:  map 37% reduce 0%
16/11/18 06:06:36 INFO mapreduce.Job:  map 38% reduce 0%
16/11/18 06:06:37 INFO mapreduce.Job:  map 40% reduce 0%
16/11/18 06:06:38 INFO mapreduce.Job:  map 41% reduce 0%
16/11/18 06:06:40 INFO mapreduce.Job:  map 43% reduce 0%
16/11/18 06:06:41 INFO mapreduce.Job:  map 44% reduce 0%
16/11/18 06:06:42 INFO mapreduce.Job:  map 46% reduce 0%
16/11/18 06:06:43 INFO mapreduce.Job:  map 48% reduce 0%
16/11/18 06:06:44 INFO mapreduce.Job:  map 49% reduce 0%
16/11/18 06:06:45 INFO mapreduce.Job:  map 50% reduce 0%
16/11/18 06:06:46 INFO mapreduce.Job:  map 52% reduce 0%
16/11/18 06:06:47 INFO mapreduce.Job:  map 53% reduce 0%
16/11/18 06:06:48 INFO mapreduce.Job:  map 54% reduce 0%
16/11/18 06:06:49 INFO mapreduce.Job:  map 56% reduce 0%
16/11/18 06:06:50 INFO mapreduce.Job:  map 58% reduce 0%
16/11/18 06:06:52 INFO mapreduce.Job:  map 60% reduce 0%
16/11/18 06:06:53 INFO mapreduce.Job:  map 62% reduce 0%
16/11/18 06:06:54 INFO mapreduce.Job:  map 63% reduce 0%
16/11/18 06:06:55 INFO mapreduce.Job:  map 64% reduce 0%
16/11/18 06:06:56 INFO mapreduce.Job:  map 66% reduce 0%
16/11/18 06:06:57 INFO mapreduce.Job:  map 67% reduce 0%
16/11/18 06:06:58 INFO mapreduce.Job:  map 69% reduce 0%
16/11/18 06:06:59 INFO mapreduce.Job:  map 70% reduce 0%
16/11/18 06:07:00 INFO mapreduce.Job:  map 71% reduce 0%
16/11/18 06:07:01 INFO mapreduce.Job:  map 73% reduce 0%
16/11/18 06:07:02 INFO mapreduce.Job:  map 75% reduce 0%
16/11/18 06:07:04 INFO mapreduce.Job:  map 77% reduce 0%
16/11/18 06:07:05 INFO mapreduce.Job:  map 79% reduce 0%
16/11/18 06:07:06 INFO mapreduce.Job:  map 80% reduce 0%
16/11/18 06:07:07 INFO mapreduce.Job:  map 81% reduce 0%
16/11/18 06:07:08 INFO mapreduce.Job:  map 83% reduce 0%
16/11/18 06:07:10 INFO mapreduce.Job:  map 86% reduce 0%
16/11/18 06:07:11 INFO mapreduce.Job:  map 87% reduce 0%
16/11/18 06:07:12 INFO mapreduce.Job:  map 88% reduce 0%
16/11/18 06:07:18 INFO mapreduce.Job:  map 95% reduce 0%
16/11/18 06:07:22 INFO mapreduce.Job:  map 98% reduce 0%
16/11/18 06:07:23 INFO mapreduce.Job:  map 100% reduce 0%
16/11/18 06:07:23 INFO mapreduce.Job: Job job_1479465422055_0005 completed successfully
16/11/18 06:07:23 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=957112
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=682
		HDFS: Number of bytes written=5120000000
		HDFS: Number of read operations=32
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=16
	Job Counters 
		Launched map tasks=8
		Other local map tasks=8
		Total time spent by all maps in occupied slots (ms)=417790
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=417790
		Total vcore-seconds taken by all map tasks=417790
		Total megabyte-seconds taken by all map tasks=427816960
	Map-Reduce Framework
		Map input records=51200000
		Map output records=51200000
		Input split bytes=682
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=3262
		CPU time spent (ms)=112170
		Physical memory (bytes) snapshot=3113594880
		Virtual memory (bytes) snapshot=22283304960
		Total committed heap usage (bytes)=2893545472
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=109963291816450258
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=5120000000

real	1m20.953s
user	0m7.100s
sys	0m0.635s
[bavaria@ip-172-31-30-5 tmp]$ 




```


dfs ls command

```
[bavaria@ip-172-31-30-5 tmp]$ hdfs dfs -ls /user/bavaria/tgen512m
Found 9 items
-rw-r--r--   3 bavaria supergroup          0 2016-11-18 06:07 /user/bavaria/tgen512m/_SUCCESS
-rw-r--r--   3 bavaria supergroup  640000000 2016-11-18 06:07 /user/bavaria/tgen512m/part-m-00000
-rw-r--r--   3 bavaria supergroup  640000000 2016-11-18 06:07 /user/bavaria/tgen512m/part-m-00001
-rw-r--r--   3 bavaria supergroup  640000000 2016-11-18 06:07 /user/bavaria/tgen512m/part-m-00002
-rw-r--r--   3 bavaria supergroup  640000000 2016-11-18 06:07 /user/bavaria/tgen512m/part-m-00003
-rw-r--r--   3 bavaria supergroup  640000000 2016-11-18 06:07 /user/bavaria/tgen512m/part-m-00004
-rw-r--r--   3 bavaria supergroup  640000000 2016-11-18 06:07 /user/bavaria/tgen512m/part-m-00005
-rw-r--r--   3 bavaria supergroup  640000000 2016-11-18 06:07 /user/bavaria/tgen512m/part-m-00006
-rw-r--r--   3 bavaria supergroup  640000000 2016-11-18 06:07 /user/bavaria/tgen512m/part-m-00007


```

Number of blocks `Total blocks (validated):	312 (avg. block size 16410256 B)`

```
[bavaria@ip-172-31-30-5 tmp]$ hadoop fsck /user/bavaria/tgen512m
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-17-8.eu-central-1.compute.internal:50070
FSCK started by bavaria (auth:SIMPLE) from /172.31.30.5 for path /user/bavaria/tgen512m at Fri Nov 18 06:08:04 EST 2016
.........Status: HEALTHY
 Total size:	5120000000 B
 Total dirs:	1
 Total files:	9
 Total symlinks:		0
 Total blocks (validated):	312 (avg. block size 16410256 B)
 Minimally replicated blocks:	312 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		3
 Number of racks:		1
FSCK ended at Fri Nov 18 06:08:04 EST 2016 in 2 milliseconds


The filesystem under path '/user/bavaria/tgen512m' is HEALTHY

```
