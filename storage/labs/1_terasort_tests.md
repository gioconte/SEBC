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

