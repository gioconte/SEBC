Running Teragen with 10GB of data and 4 mappers and block size 32 MB to with users gioconte

```
[gioconte@ip-172-31-22-224 ~]$ time hadoop jar /opt/cloudera/parcels/CDH-5.8.2-1.cdh5.8.2.p0.3/jars/hadoop-examples.jar teragen -D mapred.map.tasks=4 -Ddfs.block.size=33554432 107374182 /user/gioconte/terag_10g
16/11/15 15:16:26 INFO Configuration.deprecation: session.id is deprecated. Instead, use dfs.metrics.session-id
16/11/15 15:16:26 INFO jvm.JvmMetrics: Initializing JVM Metrics with processName=JobTracker, sessionId=
16/11/15 15:16:26 INFO terasort.TeraSort: Generating 107374182 using 1
16/11/15 15:16:26 INFO mapreduce.JobSubmitter: number of splits:1
16/11/15 15:16:26 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
16/11/15 15:16:26 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
16/11/15 15:16:26 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_local1448932334_0001
16/11/15 15:16:26 INFO mapreduce.Job: The url to track the job: http://localhost:8080/
16/11/15 15:16:26 INFO mapreduce.Job: Running job: job_local1448932334_0001
16/11/15 15:16:26 INFO mapred.LocalJobRunner: OutputCommitter set in config null
16/11/15 15:16:26 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
16/11/15 15:16:26 INFO mapred.LocalJobRunner: OutputCommitter is org.apache.hadoop.mapreduce.lib.output.FileOutputCommitter
16/11/15 15:16:26 INFO mapred.LocalJobRunner: Waiting for map tasks
16/11/15 15:16:26 INFO mapred.LocalJobRunner: Starting task: attempt_local1448932334_0001_m_000000_0
16/11/15 15:16:26 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
16/11/15 15:16:26 INFO mapred.Task:  Using ResourceCalculatorProcessTree : [ ]
16/11/15 15:16:26 INFO mapred.MapTask: Processing split: org.apache.hadoop.examples.terasort.TeraGen$RangeInputFormat$RangeInputSplit@29f9b99d
16/11/15 15:16:27 INFO mapreduce.Job: Job job_local1448932334_0001 running in uber mode : false
16/11/15 15:16:27 INFO mapreduce.Job:  map 0% reduce 0%
16/11/15 15:16:32 INFO mapred.LocalJobRunner: map > map
16/11/15 15:16:33 INFO mapreduce.Job:  map 5% reduce 0%
16/11/15 15:16:35 INFO mapred.LocalJobRunner: map > map
16/11/15 15:16:36 INFO mapreduce.Job:  map 7% reduce 0%
16/11/15 15:16:38 INFO mapred.LocalJobRunner: map > map
16/11/15 15:16:39 INFO mapreduce.Job:  map 10% reduce 0%
16/11/15 15:16:41 INFO mapred.LocalJobRunner: map > map
16/11/15 15:16:42 INFO mapreduce.Job:  map 13% reduce 0%
16/11/15 15:16:44 INFO mapred.LocalJobRunner: map > map
16/11/15 15:16:45 INFO mapreduce.Job:  map 14% reduce 0%
16/11/15 15:16:47 INFO mapred.LocalJobRunner: map > map
16/11/15 15:16:50 INFO mapred.LocalJobRunner: map > map
16/11/15 15:16:51 INFO mapreduce.Job:  map 16% reduce 0%

....

16/11/15 15:21:21 INFO mapreduce.Job:  map 92% reduce 0%
16/11/15 15:21:23 INFO mapred.LocalJobRunner: map > map
16/11/15 15:21:24 INFO mapreduce.Job:  map 94% reduce 0%
16/11/15 15:21:26 INFO mapred.LocalJobRunner: map > map
16/11/15 15:21:27 INFO mapreduce.Job:  map 96% reduce 0%
16/11/15 15:21:29 INFO mapred.LocalJobRunner: map > map
16/11/15 15:21:30 INFO mapreduce.Job:  map 97% reduce 0%
16/11/15 15:21:32 INFO mapred.LocalJobRunner: map > map
16/11/15 15:21:33 INFO mapreduce.Job:  map 99% reduce 0%
16/11/15 15:21:34 INFO mapred.LocalJobRunner: map > map
16/11/15 15:21:35 INFO mapred.Task: Task:attempt_local1448932334_0001_m_000000_0 is done. And is in the process of committing
16/11/15 15:21:35 INFO mapred.LocalJobRunner: map > map
16/11/15 15:21:35 INFO mapred.Task: Task attempt_local1448932334_0001_m_000000_0 is allowed to commit now
16/11/15 15:21:35 INFO output.FileOutputCommitter: Saved output of task 'attempt_local1448932334_0001_m_000000_0' to hdfs://ip-172-31-19-14.eu-central-1.compute.internal:8020/user/gioconte/terag_10g/_temporary/0/task_local1448932334_0001_m_000000
16/11/15 15:21:35 INFO mapred.LocalJobRunner: map
16/11/15 15:21:35 INFO mapred.Task: Task 'attempt_local1448932334_0001_m_000000_0' done.
16/11/15 15:21:35 INFO mapred.LocalJobRunner: Finishing task: attempt_local1448932334_0001_m_000000_0
16/11/15 15:21:35 INFO mapred.LocalJobRunner: map task executor complete.
16/11/15 15:21:35 INFO mapreduce.Job:  map 100% reduce 0%
16/11/15 15:21:35 INFO mapreduce.Job: Job job_local1448932334_0001 completed successfully
16/11/15 15:21:35 INFO mapreduce.Job: Counters: 21
	File System Counters
		FILE: Number of bytes read=276330
		FILE: Number of bytes written=567393
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=0
		HDFS: Number of bytes written=10737418200
		HDFS: Number of read operations=4
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=3
	Map-Reduce Framework
		Map input records=107374182
		Map output records=107374182
		Input split bytes=83
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=1420
		Total committed heap usage (bytes)=171442176
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=230593859918397906
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=10737418200

real	5m12.416s
user	2m12.218s
sys	0m10.896s
```


Running Terasort on the data previously generated

```
time hadoop jar /opt/cloudera/parcels/CDH-5.8.2-1.cdh5.8.2.p0.3/jars/hadoop-examples.jar terasort /user/gioconte/terag_10g /user/gioconte/sorted_10g
16/11/15 15:25:20 INFO terasort.TeraSort: starting
16/11/15 15:25:21 INFO input.FileInputFormat: Total input paths to process : 1
Spent 281ms computing base-splits.
Spent 8ms computing TeraScheduler splits.
Computing input splits took 290ms
Sampling 10 splits of 320
Making 1 from 100000 sampled records
Computing parititions took 679ms
Spent 972ms computing partitions.
16/11/15 15:25:22 INFO Configuration.deprecation: session.id is deprecated. Instead, use dfs.metrics.session-id
16/11/15 15:25:22 INFO jvm.JvmMetrics: Initializing JVM Metrics with processName=JobTracker, sessionId=
16/11/15 15:25:23 INFO mapreduce.JobSubmitter: number of splits:320
16/11/15 15:25:23 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_local983393903_0001
16/11/15 15:25:23 INFO mapred.LocalDistributedCacheManager: Creating symlink: /tmp/hadoop-gioconte/mapred/local/1479242303310/_partition.lst <- /home/gioconte/_partition.lst
16/11/15 15:25:23 INFO mapred.LocalDistributedCacheManager: Localized hdfs://ip-172-31-19-14.eu-central-1.compute.internal:8020/user/gioconte/sorted_tmp/_partition.lst as file:/tmp/hadoop-gioconte/mapred/local/1479242303310/_partition.lst
16/11/15 15:25:23 INFO mapreduce.Job: The url to track the job: http://localhost:8080/
16/11/15 15:25:23 INFO mapreduce.Job: Running job: job_local16547925_0001
16/11/15 15:25:23 INFO mapred.LocalJobRunner: OutputCommitter set in config null
16/11/15 15:25:23 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
16/11/15 15:25:23 INFO mapred.LocalJobRunner: OutputCommitter is org.apache.hadoop.mapreduce.lib.output.FileOutputCommitter
16/11/15 15:25:23 INFO mapred.LocalJobRunner: Starting task: attempt_local16547925_0001_m_000000_0
16/11/15 15:25:23 INFO mapred.LocalJobRunner: Waiting for map tasks
16/11/15 15:25:23 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
16/11/15 15:25:23 INFO mapred.Task:  Using ResourceCalculatorProcessTree : [ ]
16/11/15 15:25:23 INFO mapred.MapTask: Processing split: hdfs://ip-172-31-19-14.eu-central-1.compute.internal:8020/user/gioconte/terag_10g/part-m-00000:0+33554432
16/11/15 15:25:23 INFO mapred.MapTask: (EQUATOR) 0 kvi 26214396(104857584)
16/11/15 15:25:23 INFO mapred.MapTask: mapreduce.task.io.sort.mb: 100
16/11/15 15:25:23 INFO mapred.MapTask: soft limit at 83886080
16/11/15 15:25:23 INFO mapred.MapTask: bufstart = 0; bufvoid = 104857600
16/11/15 15:25:23 INFO mapred.MapTask: kvstart = 26214396; length = 6553600
16/11/15 15:25:23 INFO mapred.MapTask: Map output collector class = org.apache.hadoop.mapred.MapTask$MapOutputBuffer
16/11/15 15:25:24 INFO mapred.LocalJobRunner: 
16/11/15 15:25:24 INFO mapred.MapTask: Starting flush of map output
16/11/15 15:25:24 INFO mapred.MapTask: Spilling map output
16/11/15 15:25:24 INFO mapred.MapTask: bufstart = 0; bufend = 34225590; bufvoid = 104857600
16/11/15 15:25:24 INFO mapred.MapTask: kvstart = 26214396(104857584); kvend = 24872220(99488880); length = 1342177/6553600
16/11/15 15:25:24 INFO mapreduce.Job: Job job_local16547925_0001 running in uber mode : false
16/11/15 15:25:24 INFO mapreduce.Job:  map 0% reduce 0%

16/11/15 15:36:44 INFO mapreduce.Job:  map 100% reduce 99%
16/11/15 15:36:47 INFO mapred.LocalJobRunner: reduce > reduce
16/11/15 15:36:50 INFO mapred.LocalJobRunner: reduce > reduce
16/11/15 15:36:50 INFO mapreduce.Job:  map 100% reduce 100%
16/11/15 15:36:50 INFO mapred.Task: Task:attempt_local16547925_0001_r_000000_0 is done. And is in the process of committing
16/11/15 15:36:51 INFO mapred.LocalJobRunner: reduce > reduce
16/11/15 15:36:51 INFO mapred.Task: Task attempt_local16547925_0001_r_000000_0 is allowed to commit now
16/11/15 15:36:51 INFO output.FileOutputCommitter: Saved output of task 'attempt_local16547925_0001_r_000000_0' to hdfs://ip-172-31-19-14.eu-central-1.compute.internal:8020/user/gioconte/sorted_10g/_temporary/0/task_local16547925_0001_r_000000
16/11/15 15:36:51 INFO mapred.LocalJobRunner: reduce > reduce
16/11/15 15:36:51 INFO mapred.Task: Task 'attempt_local16547925_0001_r_000000_0' done.
16/11/15 15:36:51 INFO mapred.LocalJobRunner: Finishing task: attempt_local16547925_0001_r_000000_0
16/11/15 15:36:51 INFO mapred.LocalJobRunner: reduce task executor complete.
16/11/15 15:36:51 INFO mapreduce.Job: Job job_local16547925_0001 completed successfully
16/11/15 15:36:51 INFO mapreduce.Job: Counters: 35
	File System Counters
		FILE: Number of bytes read=33557947065
		FILE: Number of bytes written=1825727387169
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=1737303062200
		HDFS: Number of bytes written=10737418200
		HDFS: Number of read operations=111388
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=644
	Map-Reduce Framework
		Map input records=107374182
		Map output records=107374182
		Map output bytes=10952166564
		Map output materialized bytes=11166916848
		Input split bytes=50880
		Combine input records=0
		Combine output records=0
		Reduce input groups=107374182
		Reduce shuffle bytes=11166916848
		Reduce input records=107374182
		Reduce output records=107374182
		Spilled Records=319438188
		Shuffled Maps =320
		Failed Shuffles=0
		Merged Map outputs=320
		GC time elapsed (ms)=45019
		Total committed heap usage (bytes)=85532344320
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
16/11/15 15:36:51 INFO terasort.TeraSort: done

real	13m24.340s
user	12m14.493s
sys	1m42.692s
```
