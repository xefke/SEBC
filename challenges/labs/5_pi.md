# PI
Command:
```
time /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 50 100
```
Output:
```
Number of Maps  = 50
Samples per Map = 100
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Wrote input for Map #10
Wrote input for Map #11
Wrote input for Map #12
Wrote input for Map #13
Wrote input for Map #14
Wrote input for Map #15
Wrote input for Map #16
Wrote input for Map #17
Wrote input for Map #18
Wrote input for Map #19
Wrote input for Map #20
Wrote input for Map #21
Wrote input for Map #22
Wrote input for Map #23
Wrote input for Map #24
Wrote input for Map #25
Wrote input for Map #26
Wrote input for Map #27
Wrote input for Map #28
Wrote input for Map #29
Wrote input for Map #30
Wrote input for Map #31
Wrote input for Map #32
Wrote input for Map #33
Wrote input for Map #34
Wrote input for Map #35
Wrote input for Map #36
Wrote input for Map #37
Wrote input for Map #38
Wrote input for Map #39
Wrote input for Map #40
Wrote input for Map #41
Wrote input for Map #42
Wrote input for Map #43
Wrote input for Map #44
Wrote input for Map #45
Wrote input for Map #46
Wrote input for Map #47
Wrote input for Map #48
Wrote input for Map #49
Starting Job
17/08/11 09:25:29 INFO client.RMProxy: Connecting to ResourceManager at node101.sebc/10.1.1.101:8032
17/08/11 09:25:29 INFO hdfs.DFSClient: Created token for igneous: HDFS_DELEGATION_TOKEN owner=igneous@XEFKE.PA, renewer=yarn, realUser=, issueDate=1502443529580, maxDate=1503048329580, sequenceNumber=2, masterKeyId=2 on 10.1.1.101:8020
17/08/11 09:25:29 INFO security.TokenCache: Got dt for hdfs://node101.sebc:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.1.1.101:8020, Ident: (token for igneous: HDFS_DELEGATION_TOKEN owner=igneous@XEFKE.PA, renewer=yarn, realUser=, issueDate=1502443529580, maxDate=1503048329580, sequenceNumber=2, masterKeyId=2)
17/08/11 09:25:29 INFO input.FileInputFormat: Total input paths to process : 50
17/08/11 09:25:29 INFO mapreduce.JobSubmitter: number of splits:50
17/08/11 09:25:30 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502442764503_0001
17/08/11 09:25:30 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.1.1.101:8020, Ident: (token for igneous: HDFS_DELEGATION_TOKEN owner=igneous@XEFKE.PA, renewer=yarn, realUser=, issueDate=1502443529580, maxDate=1503048329580, sequenceNumber=2, masterKeyId=2)
17/08/11 09:25:31 INFO impl.YarnClientImpl: Submitted application application_1502442764503_0001
17/08/11 09:25:31 INFO mapreduce.Job: The url to track the job: http://node101.sebc:8088/proxy/application_1502442764503_0001/
17/08/11 09:25:31 INFO mapreduce.Job: Running job: job_1502442764503_0001
17/08/11 09:25:41 INFO mapreduce.Job: Job job_1502442764503_0001 running in uber mode : false
17/08/11 09:25:41 INFO mapreduce.Job:  map 0% reduce 0%
17/08/11 09:25:49 INFO mapreduce.Job:  map 4% reduce 0%
17/08/11 09:25:53 INFO mapreduce.Job:  map 8% reduce 0%
17/08/11 09:25:55 INFO mapreduce.Job:  map 16% reduce 0%
17/08/11 09:25:56 INFO mapreduce.Job:  map 18% reduce 0%
17/08/11 09:25:59 INFO mapreduce.Job:  map 22% reduce 0%
17/08/11 09:26:01 INFO mapreduce.Job:  map 26% reduce 0%
17/08/11 09:26:04 INFO mapreduce.Job:  map 32% reduce 0%
17/08/11 09:26:05 INFO mapreduce.Job:  map 36% reduce 0%
17/08/11 09:26:07 INFO mapreduce.Job:  map 40% reduce 0%
17/08/11 09:26:11 INFO mapreduce.Job:  map 44% reduce 0%
17/08/11 09:26:12 INFO mapreduce.Job:  map 50% reduce 0%
17/08/11 09:26:13 INFO mapreduce.Job:  map 54% reduce 0%
17/08/11 09:26:17 INFO mapreduce.Job:  map 58% reduce 0%
17/08/11 09:26:19 INFO mapreduce.Job:  map 62% reduce 0%
17/08/11 09:26:20 INFO mapreduce.Job:  map 68% reduce 0%
17/08/11 09:26:23 INFO mapreduce.Job:  map 72% reduce 0%
17/08/11 09:26:25 INFO mapreduce.Job:  map 76% reduce 0%
17/08/11 09:26:27 INFO mapreduce.Job:  map 80% reduce 0%
17/08/11 09:26:28 INFO mapreduce.Job:  map 82% reduce 0%
17/08/11 09:26:29 INFO mapreduce.Job:  map 86% reduce 0%
17/08/11 09:26:31 INFO mapreduce.Job:  map 90% reduce 0%
17/08/11 09:26:35 INFO mapreduce.Job:  map 92% reduce 0%
17/08/11 09:26:36 INFO mapreduce.Job:  map 100% reduce 0%
17/08/11 09:26:37 INFO mapreduce.Job:  map 100% reduce 100%
17/08/11 09:26:37 INFO mapreduce.Job: Job job_1502442764503_0001 completed successfully
17/08/11 09:26:38 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=264
		FILE: Number of bytes written=6347161
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=13540
		HDFS: Number of bytes written=215
		HDFS: Number of read operations=203
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=3
	Job Counters
		Launched map tasks=50
		Launched reduce tasks=1
		Data-local map tasks=50
		Total time spent by all maps in occupied slots (ms)=308470
		Total time spent by all reduces in occupied slots (ms)=6786
		Total time spent by all map tasks (ms)=308470
		Total time spent by all reduce tasks (ms)=6786
		Total vcore-seconds taken by all map tasks=308470
		Total vcore-seconds taken by all reduce tasks=6786
		Total megabyte-seconds taken by all map tasks=315873280
		Total megabyte-seconds taken by all reduce tasks=6948864
	Map-Reduce Framework
		Map input records=50
		Map output records=100
		Map output bytes=900
		Map output materialized bytes=1700
		Input split bytes=7640
		Combine input records=0
		Combine output records=0
		Reduce input groups=2
		Reduce shuffle bytes=1700
		Reduce input records=100
		Reduce output records=0
		Spilled Records=200
		Shuffled Maps =50
		Failed Shuffles=0
		Merged Map outputs=50
		GC time elapsed (ms)=1997
		CPU time spent (ms)=37610
		Physical memory (bytes) snapshot=22769680384
		Virtual memory (bytes) snapshot=79821189120
		Total committed heap usage (bytes)=26598703104
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters
		Bytes Read=5900
	File Output Format Counters
		Bytes Written=97
Job Finished in 68.685 seconds
Estimated value of Pi is 3.14160000000000000000

real	1m12.907s
user	0m6.531s
sys	0m0.791s
```