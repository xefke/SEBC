# List yum.repos.d:
Command:
```
ls /etc/yum.repos.d
```
Output:
```
CentOS-Base.repo       CentOS-Media.repo  cloudera-manager.repo  mysql-community-source.repo
CentOS-Debuginfo.repo  CentOS-Vault.repo  mysql-community.repo
```

# Prepare database script:

On the database host create temp user: (Node101)
```
mysql> grant all on *.* to 'temp'@'%' identified by 'temp' with grant option;
Query OK, 0 rows affected (0.01 sec)
```

On the CM host: (Node102)
Command:
```
/usr/share/cmf/schema/scm_prepare_database.sh mysql -h node101.sebc -utemp -ptemp --scm-host node102.sebc scm scm scm
```
Output:
```
[root@node102 ~]# /usr/share/cmf/schema/scm_prepare_database.sh mysql -h node101.sebc -utemp -ptemp --scm-host node102.sebc scm scm scm
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
log4j:ERROR Could not find value for key log4j.appender.A
log4j:ERROR Could not instantiate appender named "A".
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
log4j:ERROR Could not find value for key log4j.appender.A
log4j:ERROR Could not instantiate appender named "A".
[2017-08-11 07:50:23,974] INFO     0[main] - com.cloudera.enterprise.dbutil.DbCommandExecutor.testDbConnection(DbCommandExecutor.java) - Successfully connected to database.
All done, your SCM database is configured correctly!
```

Afterwards, drop temp user: (node101)
```
mysql> drop user 'temp'@'%';
Query OK, 0 rows affected (0.00 sec)
```

Verified database:
```
mysql> show databases;
```
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
| scm                |
+--------------------+
10 rows in set (0.00 sec)
```
