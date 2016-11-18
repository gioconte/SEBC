teragen
```
[bavaria@ip-172-31-30-5 tmp]$ hdfs dfs -rm -r /user/bavaria/tgen512m
16/11/18 05:56:03 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-17-8.eu-central-1.compute.internal:8020/user/bavaria/tgen512m' to trash at: hdfs://ip-172-31-17-8.eu-central-1.compute.internal:8020/user/bavaria/.Trash/Current/user/bavaria/tgen512m
[bavaria@ip-172-31-30-5 tmp]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -D mapred.map.tasks=4 -Ddfs.block.size=16777216 51200000 /user/bavaria/tgen512m
16/11/18 05:56:13 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-17-8.eu-central-1.compute.internal/172.31.17.8:8032
16/11/18 05:56:13 INFO terasort.TeraSort: Generating 51200000 using 4
16/11/18 05:56:13 INFO mapreduce.JobSubmitter: number of splits:4
16/11/18 05:56:13 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
16/11/18 05:56:13 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
16/11/18 05:56:13 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1479465422055_0002
16/11/18 05:56:14 INFO impl.YarnClientImpl: Submitted application application_1479465422055_0002
16/11/18 05:56:14 INFO mapreduce.Job: The url to track the job: http://ip-172-31-17-8.eu-central-1.compute.internal:8088/proxy/application_1479465422055_0002/
16/11/18 05:56:14 INFO mapreduce.Job: Running job: job_1479465422055_0002
16/11/18 05:56:19 INFO mapreduce.Job: Job job_1479465422055_0002 running in uber mode : false
16/11/18 05:56:19 INFO mapreduce.Job:  map 0% reduce 0%
16/11/18 05:56:29 INFO mapreduce.Job:  map 15% reduce 0%
16/11/18 05:56:31 INFO mapreduce.Job:  map 23% reduce 0%
16/11/18 05:56:32 INFO mapreduce.Job:  map 28% reduce 0%
16/11/18 05:56:34 INFO mapreduce.Job:  map 30% reduce 0%
16/11/18 05:56:35 INFO mapreduce.Job:  map 32% reduce 0%
16/11/18 05:56:37 INFO mapreduce.Job:  map 34% reduce 0%
16/11/18 05:56:38 INFO mapreduce.Job:  map 36% reduce 0%
16/11/18 05:56:40 INFO mapreduce.Job:  map 38% reduce 0%
16/11/18 05:56:41 INFO mapreduce.Job:  map 40% reduce 0%
16/11/18 05:56:43 INFO mapreduce.Job:  map 42% reduce 0%
16/11/18 05:56:44 INFO mapreduce.Job:  map 44% reduce 0%
16/11/18 05:56:46 INFO mapreduce.Job:  map 46% reduce 0%
16/11/18 05:56:47 INFO mapreduce.Job:  map 48% reduce 0%
16/11/18 05:56:49 INFO mapreduce.Job:  map 50% reduce 0%
16/11/18 05:56:50 INFO mapreduce.Job:  map 52% reduce 0%
16/11/18 05:56:52 INFO mapreduce.Job:  map 54% reduce 0%
16/11/18 05:56:53 INFO mapreduce.Job:  map 56% reduce 0%
16/11/18 05:56:55 INFO mapreduce.Job:  map 59% reduce 0%
16/11/18 05:56:57 INFO mapreduce.Job:  map 60% reduce 0%
16/11/18 05:56:59 INFO mapreduce.Job:  map 62% reduce 0%
16/11/18 05:57:00 INFO mapreduce.Job:  map 63% reduce 0%
16/11/18 05:57:02 INFO mapreduce.Job:  map 65% reduce 0%
16/11/18 05:57:03 INFO mapreduce.Job:  map 67% reduce 0%
16/11/18 05:57:05 INFO mapreduce.Job:  map 69% reduce 0%
16/11/18 05:57:06 INFO mapreduce.Job:  map 71% reduce 0%
16/11/18 05:57:08 INFO mapreduce.Job:  map 73% reduce 0%
16/11/18 05:57:09 INFO mapreduce.Job:  map 76% reduce 0%
16/11/18 05:57:11 INFO mapreduce.Job:  map 79% reduce 0%
16/11/18 05:57:12 INFO mapreduce.Job:  map 82% reduce 0%
16/11/18 05:57:14 INFO mapreduce.Job:  map 85% reduce 0%
16/11/18 05:57:15 INFO mapreduce.Job:  map 87% reduce 0%
16/11/18 05:57:17 INFO mapreduce.Job:  map 89% reduce 0%
16/11/18 05:57:18 INFO mapreduce.Job:  map 91% reduce 0%
16/11/18 05:57:20 INFO mapreduce.Job:  map 94% reduce 0%
16/11/18 05:57:23 INFO mapreduce.Job:  map 97% reduce 0%
16/11/18 05:57:24 INFO mapreduce.Job:  map 98% reduce 0%
16/11/18 05:57:25 INFO mapreduce.Job:  map 100% reduce 0%
16/11/18 05:57:26 INFO mapreduce.Job: Job job_1479465422055_0002 completed successfully
16/11/18 05:57:26 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=478540
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=339
		HDFS: Number of bytes written=5120000000
		HDFS: Number of read operations=16
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=8
	Job Counters 
		Launched map tasks=4
		Other local map tasks=4
		Total time spent by all maps in occupied slots (ms)=240246
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=240246
		Total vcore-seconds taken by all map tasks=240246
		Total megabyte-seconds taken by all map tasks=246011904
	Map-Reduce Framework
		Map input records=51200000
		Map output records=51200000
		Input split bytes=339
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=626
		CPU time spent (ms)=87400
		Physical memory (bytes) snapshot=1619156992
		Virtual memory (bytes) snapshot=11142139904
		Total committed heap usage (bytes)=1364721664
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=109963291816450258
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=5120000000

real	1m15.495s
user	0m7.036s
sys	0m0.357s
[bavaria@ip-172-31-30-5 tmp]$ 


```


dfs ls command

```
[bavaria@ip-172-31-30-5 tmp]$ hdfs dfs -ls /user/bavaria/tgen512m
Found 5 items
-rw-r--r--   3 bavaria supergroup          0 2016-11-18 05:57 /user/bavaria/tgen512m/_SUCCESS
-rw-r--r--   3 bavaria supergroup 1280000000 2016-11-18 05:57 /user/bavaria/tgen512m/part-m-00000
-rw-r--r--   3 bavaria supergroup 1280000000 2016-11-18 05:57 /user/bavaria/tgen512m/part-m-00001
-rw-r--r--   3 bavaria supergroup 1280000000 2016-11-18 05:57 /user/bavaria/tgen512m/part-m-00002
-rw-r--r--   3 bavaria supergroup 1280000000 2016-11-18 05:57 /user/bavaria/tgen512m/part-m-00003

```
