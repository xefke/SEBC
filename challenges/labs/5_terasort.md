# Terasort
Command:
```
time /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort /user/nimbus/tgen /user/nimbus/tsort
```

Output:
```
17/08/11 09:30:17 INFO terasort.TeraSort: starting
17/08/11 09:30:19 INFO hdfs.DFSClient: Created token for nimbus: HDFS_DELEGATION_TOKEN owner=nimbus@XEFKE.PA, renewer=yarn, realUser=, issueDate=1502443819141, maxDate=1503048619141, sequenceNumber=3, masterKeyId=2 on 10.1.1.101:8020
17/08/11 09:30:19 INFO security.TokenCache: Got dt for hdfs://node101.sebc:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.1.1.101:8020, Ident: (token for nimbus: HDFS_DELEGATION_TOKEN owner=nimbus@XEFKE.PA, renewer=yarn, realUser=, issueDate=1502443819141, maxDate=1503048619141, sequenceNumber=3, masterKeyId=2)
17/08/11 09:30:19 INFO input.FileInputFormat: Total input paths to process : 16
Spent 406ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 411ms
Sampling 10 splits of 112
Making 6 from 100000 sampled records
Computing parititions took 873ms
Spent 1287ms computing partitions.
17/08/11 09:30:20 INFO client.RMProxy: Connecting to ResourceManager at node101.sebc/10.1.1.101:8032
17/08/11 09:30:20 INFO mapreduce.JobSubmitter: number of splits:112
17/08/11 09:30:20 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502442764503_0002
17/08/11 09:30:20 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.1.1.101:8020, Ident: (token for nimbus: HDFS_DELEGATION_TOKEN owner=nimbus@XEFKE.PA, renewer=yarn, realUser=, issueDate=1502443819141, maxDate=1503048619141, sequenceNumber=3, masterKeyId=2)
17/08/11 09:30:21 INFO impl.YarnClientImpl: Submitted application application_1502442764503_0002
17/08/11 09:30:21 INFO mapreduce.Job: The url to track the job: http://node101.sebc:8088/proxy/application_1502442764503_0002/
17/08/11 09:30:21 INFO mapreduce.Job: Running job: job_1502442764503_0002
17/08/11 09:30:30 INFO mapreduce.Job: Job job_1502442764503_0002 running in uber mode : false
17/08/11 09:30:30 INFO mapreduce.Job:  map 0% reduce 0%
17/08/11 09:30:39 INFO mapreduce.Job:  map 1% reduce 0%
17/08/11 09:30:46 INFO mapreduce.Job:  map 2% reduce 0%
17/08/11 09:30:47 INFO mapreduce.Job:  map 3% reduce 0%
17/08/11 09:30:48 INFO mapreduce.Job:  map 7% reduce 0%
17/08/11 09:30:53 INFO mapreduce.Job:  map 8% reduce 0%
17/08/11 09:30:59 INFO mapreduce.Job:  map 9% reduce 0%
17/08/11 09:31:00 INFO mapreduce.Job:  map 14% reduce 0%
17/08/11 09:31:07 INFO mapreduce.Job:  map 15% reduce 0%
17/08/11 09:31:11 INFO mapreduce.Job:  map 17% reduce 0%
17/08/11 09:31:12 INFO mapreduce.Job:  map 21% reduce 0%
17/08/11 09:31:21 INFO mapreduce.Job:  map 22% reduce 0%
17/08/11 09:31:22 INFO mapreduce.Job:  map 23% reduce 0%
17/08/11 09:31:23 INFO mapreduce.Job:  map 25% reduce 0%
17/08/11 09:31:24 INFO mapreduce.Job:  map 28% reduce 0%
17/08/11 09:31:28 INFO mapreduce.Job:  map 29% reduce 0%
17/08/11 09:31:34 INFO mapreduce.Job:  map 31% reduce 0%
17/08/11 09:31:35 INFO mapreduce.Job:  map 33% reduce 0%
17/08/11 09:31:36 INFO mapreduce.Job:  map 35% reduce 0%
17/08/11 09:31:43 INFO mapreduce.Job:  map 36% reduce 0%
17/08/11 09:31:45 INFO mapreduce.Job:  map 37% reduce 0%
17/08/11 09:31:46 INFO mapreduce.Job:  map 38% reduce 0%
17/08/11 09:31:48 INFO mapreduce.Job:  map 40% reduce 0%
17/08/11 09:31:49 INFO mapreduce.Job:  map 41% reduce 0%
17/08/11 09:31:50 INFO mapreduce.Job:  map 42% reduce 0%
17/08/11 09:31:56 INFO mapreduce.Job:  map 43% reduce 0%
17/08/11 09:31:57 INFO mapreduce.Job:  map 46% reduce 0%
17/08/11 09:32:00 INFO mapreduce.Job:  map 48% reduce 0%
17/08/11 09:32:04 INFO mapreduce.Job:  map 49% reduce 0%
17/08/11 09:32:07 INFO mapreduce.Job:  map 50% reduce 0%
17/08/11 09:32:08 INFO mapreduce.Job:  map 51% reduce 0%
17/08/11 09:32:09 INFO mapreduce.Job:  map 52% reduce 0%
17/08/11 09:32:10 INFO mapreduce.Job:  map 53% reduce 0%
17/08/11 09:32:11 INFO mapreduce.Job:  map 54% reduce 0%
17/08/11 09:32:12 INFO mapreduce.Job:  map 55% reduce 0%
17/08/11 09:32:18 INFO mapreduce.Job:  map 57% reduce 0%
17/08/11 09:32:19 INFO mapreduce.Job:  map 58% reduce 0%
17/08/11 09:32:20 INFO mapreduce.Job:  map 59% reduce 0%
17/08/11 09:32:21 INFO mapreduce.Job:  map 60% reduce 0%
17/08/11 09:32:23 INFO mapreduce.Job:  map 62% reduce 0%
17/08/11 09:32:25 INFO mapreduce.Job:  map 63% reduce 0%
17/08/11 09:32:31 INFO mapreduce.Job:  map 65% reduce 0%
17/08/11 09:32:32 INFO mapreduce.Job:  map 66% reduce 0%
17/08/11 09:32:33 INFO mapreduce.Job:  map 67% reduce 0%
17/08/11 09:32:34 INFO mapreduce.Job:  map 69% reduce 0%
17/08/11 09:32:39 INFO mapreduce.Job:  map 71% reduce 0%
17/08/11 09:32:42 INFO mapreduce.Job:  map 72% reduce 0%
17/08/11 09:32:44 INFO mapreduce.Job:  map 73% reduce 0%
17/08/11 09:32:45 INFO mapreduce.Job:  map 75% reduce 0%
17/08/11 09:32:46 INFO mapreduce.Job:  map 76% reduce 0%
17/08/11 09:32:50 INFO mapreduce.Job:  map 77% reduce 0%
17/08/11 09:32:53 INFO mapreduce.Job:  map 78% reduce 0%
17/08/11 09:32:54 INFO mapreduce.Job:  map 79% reduce 0%
17/08/11 09:32:55 INFO mapreduce.Job:  map 80% reduce 0%
17/08/11 09:32:56 INFO mapreduce.Job:  map 82% reduce 0%
17/08/11 09:33:00 INFO mapreduce.Job:  map 83% reduce 0%
17/08/11 09:33:01 INFO mapreduce.Job:  map 84% reduce 0%
17/08/11 09:33:03 INFO mapreduce.Job:  map 85% reduce 0%
17/08/11 09:33:04 INFO mapreduce.Job:  map 86% reduce 0%
17/08/11 09:33:05 INFO mapreduce.Job:  map 88% reduce 0%
17/08/11 09:33:08 INFO mapreduce.Job:  map 89% reduce 0%
17/08/11 09:33:09 INFO mapreduce.Job:  map 89% reduce 2%
17/08/11 09:33:11 INFO mapreduce.Job:  map 90% reduce 2%
17/08/11 09:33:12 INFO mapreduce.Job:  map 90% reduce 4%
17/08/11 09:33:15 INFO mapreduce.Job:  map 91% reduce 9%
17/08/11 09:33:16 INFO mapreduce.Job:  map 92% reduce 9%
17/08/11 09:33:17 INFO mapreduce.Job:  map 94% reduce 9%
17/08/11 09:33:18 INFO mapreduce.Job:  map 94% reduce 12%
17/08/11 09:33:19 INFO mapreduce.Job:  map 94% reduce 13%
17/08/11 09:33:21 INFO mapreduce.Job:  map 94% reduce 15%
17/08/11 09:33:22 INFO mapreduce.Job:  map 95% reduce 15%
17/08/11 09:33:23 INFO mapreduce.Job:  map 96% reduce 15%
17/08/11 09:33:24 INFO mapreduce.Job:  map 96% reduce 16%
17/08/11 09:33:26 INFO mapreduce.Job:  map 97% reduce 16%
17/08/11 09:33:27 INFO mapreduce.Job:  map 98% reduce 16%
17/08/11 09:33:28 INFO mapreduce.Job:  map 99% reduce 16%
17/08/11 09:33:30 INFO mapreduce.Job:  map 100% reduce 16%
17/08/11 09:33:31 INFO mapreduce.Job:  map 100% reduce 17%
17/08/11 09:33:33 INFO mapreduce.Job:  map 100% reduce 22%
17/08/11 09:33:34 INFO mapreduce.Job:  map 100% reduce 34%
17/08/11 09:33:36 INFO mapreduce.Job:  map 100% reduce 35%
17/08/11 09:33:37 INFO mapreduce.Job:  map 100% reduce 39%
17/08/11 09:33:38 INFO mapreduce.Job:  map 100% reduce 43%
17/08/11 09:33:39 INFO mapreduce.Job:  map 100% reduce 44%
17/08/11 09:33:40 INFO mapreduce.Job:  map 100% reduce 47%
17/08/11 09:33:41 INFO mapreduce.Job:  map 100% reduce 50%
17/08/11 09:33:42 INFO mapreduce.Job:  map 100% reduce 51%
17/08/11 09:33:43 INFO mapreduce.Job:  map 100% reduce 54%
17/08/11 09:33:44 INFO mapreduce.Job:  map 100% reduce 59%
17/08/11 09:33:45 INFO mapreduce.Job:  map 100% reduce 62%
17/08/11 09:33:46 INFO mapreduce.Job:  map 100% reduce 69%
17/08/11 09:33:47 INFO mapreduce.Job:  map 100% reduce 70%
17/08/11 09:33:48 INFO mapreduce.Job:  map 100% reduce 71%
17/08/11 09:33:49 INFO mapreduce.Job:  map 100% reduce 74%
17/08/11 09:33:50 INFO mapreduce.Job:  map 100% reduce 75%
17/08/11 09:33:51 INFO mapreduce.Job:  map 100% reduce 76%
17/08/11 09:33:52 INFO mapreduce.Job:  map 100% reduce 79%
17/08/11 09:33:53 INFO mapreduce.Job:  map 100% reduce 80%
17/08/11 09:33:55 INFO mapreduce.Job:  map 100% reduce 83%
17/08/11 09:33:56 INFO mapreduce.Job:  map 100% reduce 85%
17/08/11 09:33:57 INFO mapreduce.Job:  map 100% reduce 91%
17/08/11 09:33:58 INFO mapreduce.Job:  map 100% reduce 93%
17/08/11 09:34:00 INFO mapreduce.Job:  map 100% reduce 94%
17/08/11 09:34:01 INFO mapreduce.Job:  map 100% reduce 96%
17/08/11 09:34:03 INFO mapreduce.Job:  map 100% reduce 97%
17/08/11 09:34:06 INFO mapreduce.Job:  map 100% reduce 98%
17/08/11 09:34:09 INFO mapreduce.Job:  map 100% reduce 100%
17/08/11 09:34:10 INFO mapreduce.Job: Job job_1502442764503_0002 completed successfully
17/08/11 09:34:10 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=2934634228
		FILE: Number of bytes written=5822429574
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=6553613328
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=354
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=12
	Job Counters
		Launched map tasks=112
		Launched reduce tasks=6
		Data-local map tasks=112
		Total time spent by all maps in occupied slots (ms)=1040083
		Total time spent by all reduces in occupied slots (ms)=262005
		Total time spent by all map tasks (ms)=1040083
		Total time spent by all reduce tasks (ms)=262005
		Total vcore-seconds taken by all map tasks=1040083
		Total vcore-seconds taken by all reduce tasks=262005
		Total megabyte-seconds taken by all map tasks=1065044992
		Total megabyte-seconds taken by all reduce tasks=268293120
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Map output bytes=6684672000
		Map output materialized bytes=2873023768
		Input split bytes=13328
		Combine input records=0
		Combine output records=0
		Reduce input groups=65536000
		Reduce shuffle bytes=2873023768
		Reduce input records=65536000
		Reduce output records=65536000
		Spilled Records=131072000
		Shuffled Maps =672
		Failed Shuffles=0
		Merged Map outputs=672
		GC time elapsed (ms)=15892
		CPU time spent (ms)=740780
		Physical memory (bytes) snapshot=60853673984
		Virtual memory (bytes) snapshot=184654589952
		Total committed heap usage (bytes)=71557447680
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters
		Bytes Read=6553600000
	File Output Format Counters
		Bytes Written=6553600000
17/08/11 09:34:10 INFO terasort.TeraSort: done

real	3m54.326s
user	0m8.819s
sys	0m0.914s
```