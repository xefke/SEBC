## Show Database Hostname
Command:
```
mysql> select @@hostname;
```
Output:
```
+--------------+
| @@hostname   |
+--------------+
| node101.sebc |
+--------------+
1 row in set (0.00 sec)
```

## Show version
Command:
```
mysql> select version();
```
Output:
```
+-----------+
| version() |
+-----------+
| 5.5.57    |
+-----------+
1 row in set (0.00 sec)
```

## List Databases:
Command:
```
mysql> show databases;
```
Output:
```
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
+--------------------+
9 rows in set (0.00 sec)
```
Note: I did not create the SCM database, as this is done automatically later through the prepare database script for cloudera manager.

mfernest: Our documentation points to creating scm ahead of time. We do this because customers sometimes confuse creation of the database with populating the schema, which is actually a later step. Also, security on MySQL could be set to disallow database creation by a user. I suppose we suggest a practice to avoid the case where someone else manages the db server.
