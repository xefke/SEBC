# Teragen 
## Command:
```
sudo -u nimbus time /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Ddfs.blocksize=67108864 -Dmapreduce.job.maps=16 -Dmapreduce.map.memory.mb=768 65536000 /user/nimbus/tgen
```

## Output:
```
17/08/11 08:31:47 INFO client.RMProxy: Connecting to ResourceManager at node101.sebc/10.1.1.101:8032
17/08/11 08:31:48 INFO terasort.TeraSort: Generating 65536000 using 16
17/08/11 08:31:48 INFO mapreduce.JobSubmitter: number of splits:16
17/08/11 08:31:48 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502439184458_0001
17/08/11 08:31:49 INFO impl.YarnClientImpl: Submitted application application_1502439184458_0001
17/08/11 08:31:49 INFO mapreduce.Job: The url to track the job: http://node101.sebc:8088/proxy/application_1502439184458_0001/
17/08/11 08:31:49 INFO mapreduce.Job: Running job: job_1502439184458_0001
17/08/11 08:31:56 INFO mapreduce.Job: Job job_1502439184458_0001 running in uber mode : false
17/08/11 08:31:56 INFO mapreduce.Job:  map 0% reduce 0%
17/08/11 08:32:09 INFO mapreduce.Job:  map 6% reduce 0%
17/08/11 08:32:10 INFO mapreduce.Job:  map 11% reduce 0%
17/08/11 08:32:12 INFO mapreduce.Job:  map 18% reduce 0%
17/08/11 08:32:13 INFO mapreduce.Job:  map 20% reduce 0%
17/08/11 08:32:15 INFO mapreduce.Job:  map 23% reduce 0%
17/08/11 08:32:16 INFO mapreduce.Job:  map 24% reduce 0%
17/08/11 08:32:18 INFO mapreduce.Job:  map 26% reduce 0%
17/08/11 08:32:19 INFO mapreduce.Job:  map 27% reduce 0%
17/08/11 08:32:21 INFO mapreduce.Job:  map 29% reduce 0%
17/08/11 08:32:22 INFO mapreduce.Job:  map 30% reduce 0%
17/08/11 08:32:24 INFO mapreduce.Job:  map 32% reduce 0%
17/08/11 08:32:25 INFO mapreduce.Job:  map 33% reduce 0%
17/08/11 08:32:27 INFO mapreduce.Job:  map 35% reduce 0%
17/08/11 08:32:28 INFO mapreduce.Job:  map 37% reduce 0%
17/08/11 08:32:31 INFO mapreduce.Job:  map 39% reduce 0%
17/08/11 08:32:34 INFO mapreduce.Job:  map 42% reduce 0%
17/08/11 08:32:37 INFO mapreduce.Job:  map 44% reduce 0%
17/08/11 08:32:38 INFO mapreduce.Job:  map 45% reduce 0%
17/08/11 08:32:39 INFO mapreduce.Job:  map 46% reduce 0%
17/08/11 08:32:40 INFO mapreduce.Job:  map 47% reduce 0%
17/08/11 08:32:42 INFO mapreduce.Job:  map 48% reduce 0%
17/08/11 08:32:43 INFO mapreduce.Job:  map 51% reduce 0%
17/08/11 08:32:45 INFO mapreduce.Job:  map 52% reduce 0%
17/08/11 08:32:46 INFO mapreduce.Job:  map 55% reduce 0%
17/08/11 08:32:48 INFO mapreduce.Job:  map 56% reduce 0%
17/08/11 08:32:49 INFO mapreduce.Job:  map 58% reduce 0%
17/08/11 08:32:52 INFO mapreduce.Job:  map 61% reduce 0%
17/08/11 08:32:54 INFO mapreduce.Job:  map 62% reduce 0%
17/08/11 08:32:55 INFO mapreduce.Job:  map 65% reduce 0%
17/08/11 08:32:57 INFO mapreduce.Job:  map 66% reduce 0%
17/08/11 08:32:58 INFO mapreduce.Job:  map 68% reduce 0%
17/08/11 08:33:00 INFO mapreduce.Job:  map 69% reduce 0%
17/08/11 08:33:01 INFO mapreduce.Job:  map 71% reduce 0%
17/08/11 08:33:02 INFO mapreduce.Job:  map 72% reduce 0%
17/08/11 08:33:04 INFO mapreduce.Job:  map 74% reduce 0%
17/08/11 08:33:05 INFO mapreduce.Job:  map 75% reduce 0%
17/08/11 08:33:07 INFO mapreduce.Job:  map 78% reduce 0%
17/08/11 08:33:08 INFO mapreduce.Job:  map 79% reduce 0%
17/08/11 08:33:10 INFO mapreduce.Job:  map 80% reduce 0%
17/08/11 08:33:11 INFO mapreduce.Job:  map 81% reduce 0%
17/08/11 08:33:13 INFO mapreduce.Job:  map 83% reduce 0%
17/08/11 08:33:15 INFO mapreduce.Job:  map 85% reduce 0%
17/08/11 08:33:16 INFO mapreduce.Job:  map 86% reduce 0%
17/08/11 08:33:17 INFO mapreduce.Job:  map 87% reduce 0%
17/08/11 08:33:18 INFO mapreduce.Job:  map 88% reduce 0%
17/08/11 08:33:19 INFO mapreduce.Job:  map 90% reduce 0%
17/08/11 08:33:21 INFO mapreduce.Job:  map 91% reduce 0%
17/08/11 08:33:22 INFO mapreduce.Job:  map 93% reduce 0%
17/08/11 08:33:24 INFO mapreduce.Job:  map 94% reduce 0%
17/08/11 08:33:25 INFO mapreduce.Job:  map 96% reduce 0%
17/08/11 08:33:27 INFO mapreduce.Job:  map 97% reduce 0%
17/08/11 08:33:28 INFO mapreduce.Job:  map 98% reduce 0%
17/08/11 08:33:29 INFO mapreduce.Job:  map 100% reduce 0%
17/08/11 08:33:30 INFO mapreduce.Job: Job job_1502439184458_0001 completed successfully
17/08/11 08:33:30 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=1968214
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=1368
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=64
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=32
	Job Counters
		Launched map tasks=16
		Other local map tasks=16
		Total time spent by all maps in occupied slots (ms)=559016
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=559016
		Total vcore-seconds taken by all map tasks=559016
		Total megabyte-seconds taken by all map tasks=572432384
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Input split bytes=1368
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=2674
		CPU time spent (ms)=160460
		Physical memory (bytes) snapshot=4621725696
		Virtual memory (bytes) snapshot=21480443904
		Total committed heap usage (bytes)=5324668928
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=140750829423462787
	File Input Format Counters
		Bytes Read=0
	File Output Format Counters
		Bytes Written=6553600000
```

## Time:
```
5.90user 0.74system 1:45.97elapsed 6%CPU
0inputs+1120outputs (0major+61454minor)pagefaults 0swaps
```

## Result directory tgen:
```
hdfs dfs -ls /user/nimbus/tgen
```
```
Found 17 items
-rw-r--r--   3 nimbus clouds          0 2017-08-11 08:33 /user/nimbus/tgen/_SUCCESS
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:32 /user/nimbus/tgen/part-m-00000
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:32 /user/nimbus/tgen/part-m-00001
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:32 /user/nimbus/tgen/part-m-00002
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:32 /user/nimbus/tgen/part-m-00003
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:32 /user/nimbus/tgen/part-m-00004
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:32 /user/nimbus/tgen/part-m-00005
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:32 /user/nimbus/tgen/part-m-00006
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:32 /user/nimbus/tgen/part-m-00007
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:33 /user/nimbus/tgen/part-m-00008
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:33 /user/nimbus/tgen/part-m-00009
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:33 /user/nimbus/tgen/part-m-00010
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:33 /user/nimbus/tgen/part-m-00011
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:33 /user/nimbus/tgen/part-m-00012
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:33 /user/nimbus/tgen/part-m-00013
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:33 /user/nimbus/tgen/part-m-00014
-rw-r--r--   3 nimbus clouds  409600000 2017-08-11 08:33 /user/nimbus/tgen/part-m-00015
```

## Hadoop file system check:
```
hadoop fsck -blocks /user/nimbus
```
```
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://node101.sebc:50070
FSCK started by nimbus (auth:SIMPLE) from /10.1.1.101 for path /user/nimbus at Fri Aug 11 08:37:05 UTC 2017
.................Status: HEALTHY
 Total size:	6553600000 B
 Total dirs:	3
 Total files:	17
 Total symlinks:		0
 Total blocks (validated):	112 (avg. block size 58514285 B)
 Minimally replicated blocks:	112 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		3
 Number of racks:		1
FSCK ended at Fri Aug 11 08:37:05 UTC 2017 in 12 milliseconds


The filesystem under path '/user/nimbus' is HEALTHY
```