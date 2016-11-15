Created user and folder and run teragen test with 500Mb

```
[ec2-user@ip-172-31-22-224 ~]$ sudo -u hdfs hadoop jar /opt/cloudera/parcels/CDH-5.8.2-1.cdh5.8.2.p0.3/jars/hadoop-examples.jar teragen 5000000 /user/gioconte/terag_data
16/11/15 14:08:14 INFO Configuration.deprecation: session.id is deprecated. Instead, use dfs.metrics.session-id
16/11/15 14:08:14 INFO jvm.JvmMetrics: Initializing JVM Metrics with processName=JobTracker, sessionId=
16/11/15 14:08:14 INFO terasort.TeraSort: Generating 5000000 using 1
16/11/15 14:08:14 INFO mapreduce.JobSubmitter: number of splits:1
16/11/15 14:08:14 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_local1913934675_0001
16/11/15 14:08:14 INFO mapreduce.Job: The url to track the job: http://localhost:8080/
16/11/15 14:08:14 INFO mapreduce.Job: Running job: job_local1913934675_0001
16/11/15 14:08:14 INFO mapred.LocalJobRunner: OutputCommitter set in config null
16/11/15 14:08:14 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
16/11/15 14:08:14 INFO mapred.LocalJobRunner: OutputCommitter is org.apache.hadoop.mapreduce.lib.output.FileOutputCommitter
16/11/15 14:08:14 INFO mapred.LocalJobRunner: Waiting for map tasks
16/11/15 14:08:14 INFO mapred.LocalJobRunner: Starting task: attempt_local1913934675_0001_m_000000_0
16/11/15 14:08:15 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
16/11/15 14:08:15 INFO mapred.Task:  Using ResourceCalculatorProcessTree : [ ]
16/11/15 14:08:15 INFO mapred.MapTask: Processing split: org.apache.hadoop.examples.terasort.TeraGen$RangeInputFormat$RangeInputSplit@3dbcc79d
16/11/15 14:08:15 INFO mapreduce.Job: Job job_local1913934675_0001 running in uber mode : false
16/11/15 14:08:15 INFO mapreduce.Job:  map 0% reduce 0%
16/11/15 14:08:20 INFO mapred.LocalJobRunner: 
16/11/15 14:08:20 INFO mapred.Task: Task:attempt_local1913934675_0001_m_000000_0 is done. And is in the process of committing
16/11/15 14:08:20 INFO mapred.LocalJobRunner: 
16/11/15 14:08:20 INFO mapred.Task: Task attempt_local1913934675_0001_m_000000_0 is allowed to commit now
16/11/15 14:08:20 INFO output.FileOutputCommitter: Saved output of task 'attempt_local1913934675_0001_m_000000_0' to hdfs://ip-172-31-19-14.eu-central-1.compute.internal:8020/user/gioconte/terag_data/_temporary/0/task_local1913934675_0001_m_000000
16/11/15 14:08:20 INFO mapred.LocalJobRunner: map
16/11/15 14:08:20 INFO mapred.Task: Task 'attempt_local1913934675_0001_m_000000_0' done.
16/11/15 14:08:20 INFO mapred.LocalJobRunner: Finishing task: attempt_local1913934675_0001_m_000000_0
16/11/15 14:08:20 INFO mapred.LocalJobRunner: map task executor complete.
16/11/15 14:08:20 INFO mapreduce.Job:  map 100% reduce 0%
16/11/15 14:08:20 INFO mapreduce.Job: Job job_local1913934675_0001 completed successfully
16/11/15 14:08:20 INFO mapreduce.Job: Counters: 21
	File System Counters
		FILE: Number of bytes read=276329
		FILE: Number of bytes written=561047
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=0
		HDFS: Number of bytes written=500000000
		HDFS: Number of read operations=4
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=3
	Map-Reduce Framework
		Map input records=5000000
		Map output records=5000000
		Input split bytes=82
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=71
		Total committed heap usage (bytes)=187695104
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=10735710707299981
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=500000000

```
