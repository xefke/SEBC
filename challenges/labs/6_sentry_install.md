# Create a role for HttpViewer that can read the web_logs database
```
beeline> CREATE ROLE HttpViewer;
beeline> GRANT SELECT ON default.web_logs TO ROLE HttpViewer;
```

# Assign the clouds group to this role
```
beeline> GRANT ROLE HttpViewer TO GROUP clouds;
```

# Create a role for ServiceViewer that can read the customers databases
```
beeline> CREATE ROLE ServiceViewer;
beeline> GRANT SELECT ON default.customers TO ROLE ServiceViewer;
```
# Assign the rocks group to this role
```
GRANT ROLE ServiceViewer TO GROUP rocks;
```

### Verification
```
beeline> show roles;
```
```
INFO  : OK
+----------------+--+
|      role      |
+----------------+--+
| serviceviewer  |
| httpviewer     |
+----------------+--+
2 rows selected (0.104 seconds)
```

#### Kinitted as user Nimbus:
```
0: jdbc:hive2://node101.sebc:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170811095959_f0ea0a44-fc01-43cc-9980-45bf1da443bc): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170811095959_f0ea0a44-fc01-43cc-9980-45bf1da443bc); Time taken: 0.073 seconds
INFO  : Executing command(queryId=hive_20170811095959_f0ea0a44-fc01-43cc-9980-45bf1da443bc): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170811095959_f0ea0a44-fc01-43cc-9980-45bf1da443bc); Time taken: 0.128 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
| web_logs  |
+-----------+--+
1 row selected (0.299 seconds)
```

#### Kinitted as user Igneous:
```
0: jdbc:hive2://node101.sebc:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170811100202_7bc3a527-4584-4e0e-9f55-800861483d19): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170811100202_7bc3a527-4584-4e0e-9f55-800861483d19); Time taken: 0.108 seconds
INFO  : Executing command(queryId=hive_20170811100202_7bc3a527-4584-4e0e-9f55-800861483d19): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170811100202_7bc3a527-4584-4e0e-9f55-800861483d19); Time taken: 0.141 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
+------------+--+
1 row selected (0.358 seconds)
```

# Use beeline to select ten records from web_logs
```
beeline> select * from default.web_logs limit 10;
```

Result:
```
+----------------------+---------------+-----------------+----------------+---------------------+----------------+------------------------+-------------------------+------------------------+-------------------------+---------------------+---------------------+----------------------+------------------+---------------------+--------------------+--------------------+------------------+----------------------------------------------------+-----------------------+----------------------------------------------------+------------------+-----------------------+----------------------------------------------------+----------------------------------------------------+----------------------------------------------------+----------------------------+---------------------------------------+----------------+--+
|  web_logs._version_  | web_logs.app  | web_logs.bytes  | web_logs.city  | web_logs.client_ip  | web_logs.code  | web_logs.country_code  | web_logs.country_code3  | web_logs.country_name  | web_logs.device_family  | web_logs.extension  |  web_logs.latitude  |  web_logs.longitude  | web_logs.method  | web_logs.os_family  | web_logs.os_major  | web_logs.protocol  | web_logs.record  |                  web_logs.referer                  | web_logs.region_code  |                  web_logs.request                  | web_logs.subapp  |     web_logs.time     |                    web_logs.url                    |                web_logs.user_agent                 |             web_logs.user_agent_family             | web_logs.user_agent_major  |              web_logs.id              | web_logs.date  |
+----------------------+---------------+-----------------+----------------+---------------------+----------------+------------------------+-------------------------+------------------------+-------------------------+---------------------+---------------------+----------------------+------------------+---------------------+--------------------+--------------------+------------------+----------------------------------------------------+-----------------------+----------------------------------------------------+------------------+-----------------------+----------------------------------------------------+----------------------------------------------------+----------------------------------------------------+----------------------------+---------------------------------------+----------------+--+
| 1480895575515725824  | metastore     | 1041            | Singapore      | 128.199.234.236     | NULL           | SG                     | SGP                     | Singapore              | Other                   |                     | 1.2930999994277954  | 103.85579681396484   | GET              | Other               |                    | HTTP/1.1           |                  | -                                                  | 0                     | GET /metastore/table/default/sample_07 HTTP/1.1    | table            | 2014-05-04T06:35:49Z  | /metastore/table/default/sample_07                 | Mozilla/5.0 (compatible; phpservermon/3.0.1; +http://www.phpservermonitor.org) | Other                                              |                            | 8836e6ce-9a21-449f-a372-9e57641389b3  | 2015-11-18     |
| 1480895575528308736  | metastore     | 1041            | Singapore      | 128.199.234.236     | NULL           | SG                     | SGP                     | Singapore              | Other                   |                     | 1.2930999994277954  | 103.85579681396484   | GET              | Other               |                    | HTTP/1.1           |                  | -                                                  | 0                     | GET /metastore/table/default/sample_07 HTTP/1.1    | table            | 2014-05-04T06:35:50Z  | /metastore/table/default/sample_07                 | Mozilla/5.0 (compatible; phpservermon/3.0.1; +http://www.phpservermonitor.org) | Other                                              |                            | 6ddf6e38-7b83-423c-8873-39842dca2dbb  | 2015-11-18     |
| 1480895575528308737  | search        | 1041            | Singapore      | 128.199.234.236     | NULL           | SG                     | SGP                     | Singapore              | Other                   |                     | 1.2930999994277954  | 103.85579681396484   | GET              | Other               |                    | HTTP/1.1           |                  | -                                                  | 0                     | GET /search/?collection=10000001 HTTP/1.1          |                  | 2014-05-04T06:35:52Z  | /search/?collection=10000001                       | Mozilla/5.0 (compatible; phpservermon/3.0.1; +http://www.phpservermonitor.org) | Other                                              |                            | 313bb28e-dd7c-4364-a11e-9ffb0db7b303  | 2015-11-18     |
| 1480895575528308738  | search        | 1041            | Singapore      | 128.199.234.236     | NULL           | SG                     | SGP                     | Singapore              | Other                   |                     | 1.2930999994277954  | 103.85579681396484   | GET              | Other               |                    | HTTP/1.1           |                  | -                                                  | 0                     | GET /search/?collection=10000001 HTTP/1.1          |                  | 2014-05-04T06:35:53Z  | /search/?collection=10000001                       | Mozilla/5.0 (compatible; phpservermon/3.0.1; +http://www.phpservermonitor.org) | Other                                              |                            | ecb47c61-a9e4-4b59-9234-04bd57695987  | 2015-11-18     |
| 1480895575528308739  |               | 238             | Singapore      | 128.199.234.236     | NULL           | SG                     | SGP                     | Singapore              | Other                   |                     | 1.2930999994277954  | 103.85579681396484   | HEAD             | Other               |                    | HTTP/1.1           |                  | -                                                  | 0                     | HEAD / HTTP/1.1                                    |                  | 2014-05-04T06:35:54Z  | /                                                  | Mozilla/5.0 (compatible; phpservermon/3.0.1; +http://www.phpservermonitor.org) | Other                                              |                            | affdb6b9-3657-4d15-8af8-2ba2f3a69343  | 2015-11-18     |
| 1480895575528308740  | beeswax       | 1041            | Mountain View  | 66.249.76.236       | NULL           | US                     | USA                     | United States          | Spider                  |                     | 37.38600158691406   | -122.08380126953125  | GET              | Other               |                    | HTTP/1.1           |                  | -                                                  | NULL                  | GET /beeswax/query_history?q-type=beeswax&amp;q-user=dy8515s&amp;q-auto_query=off HTTP/1.1 |                  | 2014-05-04T06:35:54Z  | /beeswax/query_history?q-type=beeswax&amp;q-user=dy8515s&amp;q-auto_query=off | Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html) | Googlebot                                          | 2                          | e3f88d9e-7e5b-4ef7-8941-c0d83720616c  | 2015-11-18     |
| 1480895575528308741  |               | 1041            | Guiyang        | 222.85.131.87       | NULL           | CN                     | CHN                     | China                  | Other                   |                     | 26.58329963684082   | 106.7166976928711    | GET              | Windows 7           |                    | HTTP/1.1           |                  | -                                                  | 18                    | GET / HTTP/1.1                                     |                  | 2014-05-04T06:35:55Z  | /                                                  | Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.1; Trident/6.0) | IE                                                 | 10                         | 4dbb1f74-6856-4fe3-8515-c53eab600b60  | 2015-11-18     |
| 1480895575529357312  | desktop       | 0               | Guiyang        | 222.85.131.87       | NULL           | CN                     | CHN                     | China                  | Other                   |                     | 26.58329963684082   | 106.7166976928711    |                  | Other               |                    |                    |                  | -                                                  | 18                    | -                                                  |                  | 2014-05-04T06:36:16Z  |                                                    | -                                                  | Other                                              |                            | 86cdb56d-99c0-4701-a842-472741bb833a  | 2015-11-18     |
| 1480895575529357313  | search        | 1041            | Shanghai       | 101.226.168.225     | NULL           | CN                     | CHN                     | China                  | Other                   |                     | 31.04560089111328   | 121.39969635009766   | GET              | Windows 7           |                    | HTTP/1.1           |                  | http://demo.gethue.com/search/?collection=10000001&amp;fq=%7Cuser_statuses_count%3A%5B%229000%22%20TO%20%229999%22%5D%7Cuser_location%3A%22new%20york%22&amp;query&amp;rows=15&amp;start=0 | 23                    | GET /search/?collection=10000001&amp;fq=%7Cuser_statuses_count%3A%5B%229000%22%20TO%20%229999%22%5D%7Cuser_location%3A%22new%20york%22&amp;query&amp;rows=15&amp;start=0 HTTP/1.1 |                  | 2014-05-04T06:38:31Z  | /search/?collection=10000001&amp;fq=%7Cuser_statuses_count%3A%5B%229000%22%20TO%20%229999%22%5D%7Cuser_location%3A%22new%20york%22&amp;query&amp;rows=15&amp;start=0 | "Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.1 (KHTML |  like Gecko) Chrome/21.0.1180.89 Safari/537.1; 360Spider" | Chrome                     | 21                                    | 2015-11-18     |
| 1480895575529357314  | search        | 1041            | Mountain View  | 66.249.76.225       | NULL           | US                     | USA                     | United States          | Spider                  |                     | 37.38600158691406   | -122.08380126953125  | GET              | Other               |                    | HTTP/1.1           |                  | -                                                  | NULL                  | GET /search/?collection=10000001&amp;query=&amp;fq=%7Cuser_followers_count%3A%5B%22100%22%20TO%20%22199%22%5D%7Cuser_location%3A%22philippines%22&amp;rows=15&amp;start=240 HTTP/1.1 |                  | 2014-05-04T06:38:55Z  | /search/?collection=10000001&amp;query=&amp;fq=%7Cuser_followers_count%3A%5B%22100%22%20TO%20%22199%22%5D%7Cuser_location%3A%22philippines%22&amp;rows=15&amp;start=240 | Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html) | Googlebot                                          | 2                          | 8260ca42-55d6-4cd4-8beb-8767826dc929  | 2015-11-18     |
+----------------------+---------------+-----------------+----------------+---------------------+----------------+------------------------+-------------------------+------------------------+-------------------------+---------------------+---------------------+----------------------+------------------+---------------------+--------------------+--------------------+------------------+----------------------------------------------------+-----------------------+----------------------------------------------------+------------------+-----------------------+----------------------------------------------------+----------------------------------------------------+----------------------------------------------------+----------------------------+---------------------------------------+----------------+--+
10 rows selected (0.405 seconds)
```

# Use beeswax to select ten records from customers
