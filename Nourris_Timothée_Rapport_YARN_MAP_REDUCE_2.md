Nourris Timothée Rapport Lab YARN AND MAP REDUCE II


1.6.3 Run the job

Start the wordcount job using the JAR that we send to the edge node. Referer
to previous labs for the command.

First, we need to see where our .jar file is with filezilla
sftp://t.nourris@hadoop-edge01.efrei.online/home/t.nourris/hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar


Output:

[t.nourris@hadoop-edge01 ~]$ alias launch_job="yarn jar hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar"
[t.nourris@hadoop-edge01 ~]$ launch_job wordcount trees.csv count
21/10/04 20:35:23 INFO impl.TimelineReaderClientImpl: Initialized TimelineReader URI=https://hadoop-master03.efrei.online:8199/ws/v2/timeline/, clusterId=yarn-cluster
21/10/04 20:35:24 INFO client.AHSProxy: Connecting to Application History server at hadoop-master03.efrei.online/163.172.102.23:10200
21/10/04 20:35:24 INFO hdfs.DFSClient: Created token for t.nourris: HDFS_DELEGATION_TOKEN owner=t.nourris@EFREI.ONLINE, renewer=yarn, realUser=, issueDate=1633372524151, maxDate=1633977324151, sequenceNumber=2796, masterKeyId=47 on ha-hdfs:efrei
21/10/04 20:35:24 INFO security.TokenCache: Got dt for hdfs://efrei; Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:efrei, Ident: (token for t.nourris: HDFS_DELEGATION_TOKEN owner=t.nourris@EFREI.ONLINE, renewer=yarn, realUser=, issueDate=1633372524151, maxDate=1633977324151, sequenceNumber=2796, masterKeyId=47)
21/10/04 20:35:24 INFO client.ConfiguredRMFailoverProxyProvider: Failing over to rm2
21/10/04 20:35:24 INFO mapreduce.JobResourceUploader: Disabling Erasure Coding for path: /user/t.nourris/.staging/job_1630864376208_1930
21/10/04 20:35:25 INFO input.FileInputFormat: Total input files to process : 1
21/10/04 20:35:25 INFO mapreduce.JobSubmitter: number of splits:1
21/10/04 20:35:25 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1630864376208_1930
21/10/04 20:35:25 INFO mapreduce.JobSubmitter: Executing with tokens: [Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:efrei, Ident: (token for t.nourris: HDFS_DELEGATION_TOKEN owner=t.nourris@EFREI.ONLINE, renewer=yarn, realUser=, issueDate=1633372524151, maxDate=1633977324151, sequenceNumber=2796, masterKeyId=47)]
21/10/04 20:35:25 INFO conf.Configuration: found resource resource-types.xml at file:/etc/hadoop/1.0.3.0-223/0/resource-types.xml
21/10/04 20:35:25 INFO impl.TimelineClientImpl: Timeline service address: hadoop-master03.efrei.online:8190
21/10/04 20:35:26 INFO impl.YarnClientImpl: Submitted application application_1630864376208_1930
21/10/04 20:35:26 INFO mapreduce.Job: The url to track the job: https://hadoop-master02.efrei.online:8090/proxy/application_1630864376208_1930/
21/10/04 20:35:26 INFO mapreduce.Job: Running job: job_1630864376208_1930
21/10/04 20:35:35 INFO mapreduce.Job: Job job_1630864376208_1930 running in uber mode : false
21/10/04 20:35:35 INFO mapreduce.Job:  map 0% reduce 0%
21/10/04 20:35:44 INFO mapreduce.Job:  map 100% reduce 0%
21/10/04 20:35:49 INFO mapreduce.Job:  map 100% reduce 100%
21/10/04 20:35:49 INFO mapreduce.Job: Job job_1630864376208_1930 completed successfully
21/10/04 20:35:49 INFO mapreduce.Job: Counters: 54
        File System Counters
                FILE: Number of bytes read=107379
                FILE: Number of bytes written=740745
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=171007
                HDFS: Number of bytes written=93481
                HDFS: Number of read operations=8
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=2
                HDFS: Number of bytes read erasure-coded=0
        Job Counters
                Launched map tasks=1
                Launched reduce tasks=1
                Data-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=19023
                Total time spent by all reduces in occupied slots (ms)=9696
                Total time spent by all map tasks (ms)=6341
                Total time spent by all reduce tasks (ms)=2424
                Total vcore-milliseconds taken by all map tasks=6341
                Total vcore-milliseconds taken by all reduce tasks=2424
                Total megabyte-milliseconds taken by all map tasks=9739776
                Total megabyte-milliseconds taken by all reduce tasks=4964352
        Map-Reduce Framework
                Map input records=1793
                Map output records=10056
                Map output bytes=199948
                Map output materialized bytes=107379
                Input split bytes=102
                Combine input records=10056
                Combine output records=3487
                Reduce input groups=3487
                Reduce shuffle bytes=107379
                Reduce input records=3487
                Reduce output records=3487
                Spilled Records=6974
                Shuffled Maps =1
                Failed Shuffles=0
                Merged Map outputs=1
                GC time elapsed (ms)=167
                CPU time spent (ms)=3370
                Physical memory (bytes) snapshot=1460649984
                Virtual memory (bytes) snapshot=7291101184
                Total committed heap usage (bytes)=1499463680
                Peak Map Physical memory (bytes)=1162145792
                Peak Map Virtual memory (bytes)=3404529664
                Peak Reduce Physical memory (bytes)=298504192
                Peak Reduce Virtual memory (bytes)=3886571520
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=170905
        File Output Format Counters
                Bytes Written=93481
 

1.7 How will the lab work?
1.7.1 Important 1

This lab will last at least 2 weeks and there are all kinds of exercises, easy and
hard. So start with all the easy exercises, you will do the hard ones next time.

If you start with the difficult ones and you have no experience, you are going to have problems. You do as you want, it’s up to you.

For each of these projects, if you can’t do everything that is asked for, try
to get closer. The scoring takes into account your attempts.


1.7.2 Important 2
Don’t forget to write unit test if you want bonus points. Here some documentation about it.
1.7.3 Important 3
If you don’t have a GitHub account, you must create one. You must clone the
base repository following this tutorial (keep your repository public).

Account created with gitbash at C:\Cours\M1\S7\Big Data Frameworks I\BigDataFramework


We check if we have the file trees.csv
Output :
[t.nourris@hadoop-edge01 ~]$ ls
20417.txt.utf-8  5000-8.txt                                                        local.txt  reducer.py  trees.csv
4300-0.txt       hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar  mapper.py  sudoku.dta

Now we need to put it in hdfs 

Output :
[t.nourris@hadoop-edge01 ~]$ hdfs dfs -copyFromLocal trees.csv
[t.nourris@hadoop-edge01 ~]$ hdfs dfs -ls
Found 9 items
drwx------   - t.nourris t.nourris          0 2021-09-08 02:00 .Trash
drwx------   - t.nourris t.nourris          0 2021-09-24 16:09 .staging
drwxr-xr-x   - t.nourris t.nourris          0 2021-09-24 15:14 10GB-sort-input
drwxr-xr-x   - t.nourris t.nourris          0 2021-09-24 16:06 10GB-sort-output
drwxr-xr-x   - t.nourris t.nourris          0 2021-09-24 16:09 10GB-sort-validate
-rw-r--r--   3 t.nourris t.nourris     798774 2021-09-09 17:56 1342-0.txt
drwxr-xr-x   - t.nourris t.nourris          0 2021-09-27 22:31 gutenberg
drwxr-xr-x   - t.nourris t.nourris          0 2021-09-09 17:58 raw
-rw-r--r--   3 t.nourris t.nourris     170905 2021-09-30 19:55 trees.csv

1.8.1 Districts containing trees (very easy)

Write a MapReduce job that displays the list of distinct containing trees in this
file. Obviously, it’s twenty or less different arrondissements, but exactly how
many?

You just need to put rounding as a key and put any value or NullWritable
as a value, output from the mapper.
The reducer will just have to output the keys and values it receives, it doesn’t
even have to loop through the values since it ignores them.

# TreesMapper:

package com.opstty.mapper;

import org.apache.hadoop.io.IntWritable;
import org.apache.hadoop.io.Text;
import org.apache.hadoop.mapreduce.Mapper;
import java.io.IOException;

public class TreesMapper extends Mapper<Object, Text, IntWritable, IntWritable> {
    public int c_line = 0;
    public void map(Object key, Text value, Context context) throws IOException, InterruptedException {
        if (c_line != 0) {
            context.write(new IntWritable(Integer.parseInt(value.toString().split(";")[1])), new IntWritable(1));
        }
        c_line++;
    }
}


# TreesReducer:

package com.opstty.reducer;

import java.io.IOException;
import org.apache.hadoop.io.IntWritable;
import org.apache.hadoop.mapreduce.Reducer;

public class TreesReducer extends Reducer<IntWritable, IntWritable, IntWritable, IntWritable> {
    public void reduce(IntWritable key, Iterable<IntWritable> values, Context context)
            throws IOException, InterruptedException {
        int sum = 0;
        for (IntWritable val : values) {
            sum += val.get();
        }
        context.write(key, new IntWritable(sum));
    }
}


Output:
launch_job DistrictTrees trees.csv districts
21/10/04 23:24:32 INFO impl.TimelineReaderClientImpl: Initialized TimelineReader URI=https://hadoop-master03.efrei.online:8199/ws/v2/timeline/, clusterId=yarn-cluster
21/10/04 23:24:32 INFO client.AHSProxy: Connecting to Application History server at hadoop-master03.efrei.online/163.172.102.23:10200
21/10/04 23:24:32 INFO hdfs.DFSClient: Created token for t.nourris: HDFS_DELEGATION_TOKEN owner=t.nourris@EFREI.ONLINE, renewer=yarn, realUser=, issueDate=1633382672620, maxDate=1633987472620, sequenceNumber=3083, masterKeyId=47 on ha-hdfs:efrei
21/10/04 23:24:32 INFO security.TokenCache: Got dt for hdfs://efrei; Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:efrei, Ident: (token for t.nourris: HDFS_DELEGATION_TOKEN owner=t.nourris@EFREI.ONLINE, renewer=yarn, realUser=, issueDate=1633382672620, maxDate=1633987472620, sequenceNumber=3083, masterKeyId=47)
21/10/04 23:24:32 INFO client.ConfiguredRMFailoverProxyProvider: Failing over to rm2
21/10/04 23:24:32 INFO mapreduce.JobResourceUploader: Disabling Erasure Coding for path: /user/t.nourris/.staging/job_1630864376208_2106
21/10/04 23:24:33 INFO input.FileInputFormat: Total input files to process : 1
21/10/04 23:24:33 INFO mapreduce.JobSubmitter: number of splits:1
21/10/04 23:24:33 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1630864376208_2106
21/10/04 23:24:33 INFO mapreduce.JobSubmitter: Executing with tokens: [Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:efrei, Ident: (token for t.nourris: HDFS_DELEGATION_TOKEN owner=t.nourris@EFREI.ONLINE, renewer=yarn, realUser=, issueDate=1633382672620, maxDate=1633987472620, sequenceNumber=3083, masterKeyId=47)]
21/10/04 23:24:33 INFO conf.Configuration: found resource resource-types.xml at file:/etc/hadoop/1.0.3.0-223/0/resource-types.xml
21/10/04 23:24:33 INFO impl.TimelineClientImpl: Timeline service address: hadoop-master03.efrei.online:8190
21/10/04 23:24:34 INFO impl.YarnClientImpl: Submitted application application_1630864376208_2106
21/10/04 23:24:34 INFO mapreduce.Job: The url to track the job: https://hadoop-master02.efrei.online:8090/proxy/application_1630864376208_2106/
21/10/04 23:24:34 INFO mapreduce.Job: Running job: job_1630864376208_2106
21/10/04 23:24:44 INFO mapreduce.Job: Job job_1630864376208_2106 running in uber mode : false
21/10/04 23:24:44 INFO mapreduce.Job:  map 0% reduce 0%
21/10/04 23:24:52 INFO mapreduce.Job: Task Id : attempt_1630864376208_2106_m_000000_0, Status : FAILED
Error: java.lang.ArrayIndexOutOfBoundsException: 1
        at com.opstty.mapper.TreesMapper.map(TreesMapper.java:12)
        at com.opstty.mapper.TreesMapper.map(TreesMapper.java:8)
        at org.apache.hadoop.mapreduce.Mapper.run(Mapper.java:146)
        at org.apache.hadoop.mapred.MapTask.runNewMapper(MapTask.java:799)
        at org.apache.hadoop.mapred.MapTask.run(MapTask.java:347)
        at org.apache.hadoop.mapred.YarnChild$2.run(YarnChild.java:174)
        at java.security.AccessController.doPrivileged(Native Method)
        at javax.security.auth.Subject.doAs(Subject.java:422)
        at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1762)
        at org.apache.hadoop.mapred.YarnChild.main(YarnChild.java:168)

21/10/04 23:25:01 INFO mapreduce.Job: Task Id : attempt_1630864376208_2106_m_000000_1, Status : FAILED
Error: java.lang.ArrayIndexOutOfBoundsException: 1
        at com.opstty.mapper.TreesMapper.map(TreesMapper.java:12)
        at com.opstty.mapper.TreesMapper.map(TreesMapper.java:8)
        at org.apache.hadoop.mapreduce.Mapper.run(Mapper.java:146)
        at org.apache.hadoop.mapred.MapTask.runNewMapper(MapTask.java:799)
        at org.apache.hadoop.mapred.MapTask.run(MapTask.java:347)
        at org.apache.hadoop.mapred.YarnChild$2.run(YarnChild.java:174)
        at java.security.AccessController.doPrivileged(Native Method)
        at javax.security.auth.Subject.doAs(Subject.java:422)
        at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1762)
        at org.apache.hadoop.mapred.YarnChild.main(YarnChild.java:168)

21/10/04 23:25:09 INFO mapreduce.Job: Task Id : attempt_1630864376208_2106_m_000000_2, Status : FAILED
Error: java.lang.ArrayIndexOutOfBoundsException: 1
        at com.opstty.mapper.TreesMapper.map(TreesMapper.java:12)
        at com.opstty.mapper.TreesMapper.map(TreesMapper.java:8)
        at org.apache.hadoop.mapreduce.Mapper.run(Mapper.java:146)
        at org.apache.hadoop.mapred.MapTask.runNewMapper(MapTask.java:799)
        at org.apache.hadoop.mapred.MapTask.run(MapTask.java:347)
        at org.apache.hadoop.mapred.YarnChild$2.run(YarnChild.java:174)
        at java.security.AccessController.doPrivileged(Native Method)
        at javax.security.auth.Subject.doAs(Subject.java:422)
        at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1762)
        at org.apache.hadoop.mapred.YarnChild.main(YarnChild.java:168)

21/10/04 23:25:15 INFO mapreduce.Job:  map 100% reduce 100%
21/10/04 23:25:15 INFO mapreduce.Job: Job job_1630864376208_2106 failed with state FAILED due to: Task failed task_1630864376208_2106_m_000000
Job failed as tasks failed. failedMaps:1 failedReduces:0 killedMaps:0 killedReduces: 0

21/10/04 23:25:15 INFO mapreduce.Job: Counters: 10
        Job Counters
                Failed map tasks=4
                Killed reduce tasks=1
                Launched map tasks=4
                Other local map tasks=3
                Data-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=68235
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=22745
                Total vcore-milliseconds taken by all map tasks=22745
                Total megabyte-milliseconds taken by all map tasks=34936320

# Output:
[t.nourris@hadoop-edge01 ~]$ hdfs dfs -cat /user/t.nourris/districts/part-r-00000
11      1
12      29
13      2
14      3
15      1
16      36
17      1
18      1
19      6
20      3
3       1
4       1
5       2
6       1
7       3
8       5
9       1

# 1.8.2 Show all existing species (very easy)
Write a MapReduce job that displays the list of different species trees in this
file.

# Mapper:
package com.opstty.mapper;

import org.apache.hadoop.io.NullWritable;
import org.apache.hadoop.io.Text;
import org.apache.hadoop.mapreduce.Mapper;
import java.io.IOException;

public class SpeciesMapper extends Mapper<Object, Text, Text, NullWritable> {
    public int c_line = 0;

    public void map(Object key, Text value, Context context) throws IOException, InterruptedException {
        if (c_line != 0) {
            context.write(new Text(value.toString().split(";")[3]), NullWritable.get());
        }
        c_line++;
    }
}

# Reducer:
package com.opstty.reducer;

import java.io.IOException;

import org.apache.hadoop.io.NullWritable;
import org.apache.hadoop.io.Text;
import org.apache.hadoop.mapreduce.Reducer;

public class SpeciesReducer extends Reducer<Text, NullWritable, Text, NullWritable> {
    public void reduce(Text key, Iterable<NullWritable> values, Context context)
            throws IOException, InterruptedException {
        context.write(key, NullWritable.get());
    }
}

# Output:
[t.nourris@hadoop-edge01 ~]$ hdfs dfs -cat /user/t.nourris/treespecies/part-r-00000
araucana
atlantica
australis
baccata
bignonioides
biloba
bungeana
cappadocicum
carpinifolia
colurna
coulteri
decurrens
dioicus
distichum
excelsior
fraxinifolia
giganteum
giraldii
glutinosa
grandiflora
hippocastanum
ilex
involucrata
...

# 1.8.3 Number of trees by kinds (easy)
Write a MapReduce job that calculates the number of trees of each kinds.
For example, there are 3 Acer, 19 Platanus, etc. How will you define the keys
and values passed between the mapper and the reducer?
The mapper must extract the kind of tree. The reducer gets the pairs (keyI,
valueI) with the same key, so this key must be the kind of tree; the value being
the number of such trees.

# Mapper:
package com.opstty.mapper;

import org.apache.hadoop.io.IntWritable;
import org.apache.hadoop.io.Text;
import org.apache.hadoop.mapreduce.Mapper;
import java.io.IOException;

public class CountTreesMapper extends Mapper<Object, Text, Text, IntWritable> {
    public int c_line = 0;

    public void map(Object key, Text value, Context context) throws IOException, InterruptedException {
        if (c_line != 0) {
            context.write(new Text(value.toString().split(";")[3]), new IntWritable(1));
        }
        c_line++;
    }
}


# Reducer:
package com.opstty.reducer;

import java.io.IOException;

import org.apache.hadoop.io.IntWritable;
import org.apache.hadoop.io.Text;
import org.apache.hadoop.mapreduce.Reducer;

public class CountTreesReducer extends Reducer<Text, IntWritable, Text, IntWritable> {
    public void reduce(Text key, Iterable<IntWritable> values, Context context)
            throws IOException, InterruptedException {
        int sum = 0;
        for (IntWritable val : values) {
            sum += val.get();
        }
        context.write(key, new IntWritable(sum));
    }
}


# Output:
[t.nourris@hadoop-edge01 ~]$ hdfs dfs -cat /user/t.nourris/treespeciescount/part-r-00000
araucana        1
atlantica       2
australis       1
baccata 2
bignonioides    1
biloba  5
bungeana        1
cappadocicum    1
carpinifolia    4
colurna 3
coulteri        1
decurrens       1
dioicus 1
...
