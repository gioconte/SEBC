Copying ZIP into precious folder

```
[gioconte@ip-172-31-22-224 ~]$ hdfs dfs -mkdir -p /user/gioconte/precious
[gioconte@ip-172-31-22-224 tmp]$ hdfs dfs -copyFromLocal SEBC-master.zip /user/gioconte/precious
[gioconte@ip-172-31-22-224 tmp]$ hdfs dfs -ls /user/gioconte/precious
Found 1 items
-rw-r--r--   3 gioconte supergroup     410158 2016-11-15 15:49 /user/gioconte/precious/SEBC-master.zip
```


Remove file
```
[gioconte@ip-172-31-22-224 tmp]$ hdfs dfs -rm /user/gioconte/precious/SEBC-master.zip
16/11/15 15:59:01 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-19-14.eu-central-1.compute.internal:8020/user/gioconte/precious/SEBC-master.zip' to trash at: hdfs://ip-172-31-19-14.eu-central-1.compute.internal:8020/user/gioconte/.Trash/Current/user/gioconte/precious/SEBC-master.zip
[gioconte@ip-172-31-22-224 tmp]$ hdfs dfs -ls /user/gioconte/precious/.snapshot
Found 1 items
drwxr-xr-x   - gioconte supergroup          0 2016-11-15 15:53 /user/gioconte/precious/.snapshot/sebc-hdfs-test
```

Restoring the file
```
[gioconte@ip-172-31-22-224 tmp]$ hdfs dfs -cp /user/gioconte/precious/.snapshot/sebc-hdfs-test/SEBC-master.zip /user/gioconte/precious
[gioconte@ip-172-31-22-224 tmp]$ hdfs dfs -ls /user/gioconte/precious
Found 1 items
-rw-r--r--   3 gioconte supergroup     410158 2016-11-15 16:01 /user/gioconte/precious/SEBC-master.zip
```


