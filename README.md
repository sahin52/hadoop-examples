hadoop-examples
===============

Examples codes demonstrating features in Hadoop eco-system.

Running Wordcount Example
------------------------------------
```
cd /usr/local/hadoop
hadoop dfs -mkdir ~/wordcount/input
sudo vi file01
sudo vi file02
bin/hadoop dfs -copyFromLocal file01 /home/impadmin/wordcount/input/
bin/hadoop dfs -copyFromLocal file02 /home/impadmin/wordcount/input/
bin/hadoop dfs -ls /home/impadmin/wordcount/input/

Found 2 items
-rw-r--r--   1 impadmin supergroup          0 2012-05-08 14:51 /home/impadmin/wordcount/input/file01
-rw-r--r--   1 impadmin supergroup          0 2012-05-08 14:51 /home/impadmin/wordcount/input/file02

bin/hadoop jar ~/development/hadoop-examples/target/hadoop-examples-1.0.jar com.impetus.code.examples.hadoop.mapred.wordcount.WordCount /home/impadmin/wordcount/input /home/impadmin/wordcount/output
bin/hadoop dfs -ls /home/impadmin/wordcount/output/

Found 3 items
-rw-r--r--   1 impadmin supergroup          0 2012-05-08 15:23 /home/impadmin/wordcount/output/_SUCCESS
drwxr-xr-x   - impadmin supergroup          0 2012-05-08 15:22 /home/impadmin/wordcount/output/_logs
-rw-r--r--   1 impadmin supergroup         41 2012-05-08 15:23 /home/impadmin/wordcount/output/part-00000

bin/hadoop dfs -cat /home/impadmin/wordcount/output/part-00000

Bye	1
Goodbye	1
Hadoop	2
Hello	2
World	2
```
Running Weather Example
-------------------------------




http://code.google.com/p/hadoop-map-reduce-examples

