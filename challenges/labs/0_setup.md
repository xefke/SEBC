Cloud Provider: AWS

Instances: 
```
DNS Name         IP Address       External IP
--------         ----------       -----------
node101.sebc     10.1.1.101       52.213.101.240
node102.sebc     10.1.1.102       52.50.120.234
node103.sebc     10.1.1.103       34.253.75.163
node104.sebc     10.1.1.104       52.208.2.53
node105.sebc     10.1.1.105       54.72.8.53
```

Linux Release: Centos 6.5

File Sytem Capacity: (df -h)
```
ssh node101
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde       126G  801M  119G   1% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
```

Yum repolist
```
[root@node101 ~]# yum repolist enabled
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: mozart.ee.ic.ac.uk
 * extras: mirror.freethought-internet.co.uk
 * updates: mirror.vorboss.net
repo id                                    repo name                                              status
base                                       CentOS-6 - Base                                        6,706
extras                                     CentOS-6 - Extras                                         45
updates                                    CentOS-6 - Updates                                       447
repolist: 7,198
```

```
pssh -h "nodes.txt" -l root -i "-O StrictHostKeyChecking=no" "cat /etc/passwd | grep 'nimbus\|igneous'"
```
```
[1] 07:01:59 [SUCCESS] 10.1.1.101
nimbus:x:2800:501::/home/nimbus:/bin/bash
igneous:x:2900:500::/home/igneous:/bin/bash
[2] 07:01:59 [SUCCESS] 10.1.1.102
nimbus:x:2800:501::/home/nimbus:/bin/bash
igneous:x:2900:500::/home/igneous:/bin/bash
[3] 07:01:59 [SUCCESS] 10.1.1.103
nimbus:x:2800:501::/home/nimbus:/bin/bash
igneous:x:2900:500::/home/igneous:/bin/bash
[4] 07:01:59 [SUCCESS] 10.1.1.104
nimbus:x:2800:501::/home/nimbus:/bin/bash
igneous:x:2900:500::/home/igneous:/bin/bash
[5] 07:01:59 [SUCCESS] 10.1.1.105
nimbus:x:2800:501::/home/nimbus:/bin/bash
igneous:x:2900:500::/home/igneous:/bin/bash
```

```
pssh -h "nodes.txt" -l root -i "-O StrictHostKeyChecking=no" "cat /etc/group | grep 'rocks\|clouds'"
```
```
[1] 07:03:35 [SUCCESS] 10.1.1.101
rocks:x:500:
clouds:x:501:
[2] 07:03:35 [SUCCESS] 10.1.1.103
rocks:x:500:
clouds:x:501:
[3] 07:03:35 [SUCCESS] 10.1.1.102
rocks:x:500:
clouds:x:501:
[4] 07:03:35 [SUCCESS] 10.1.1.105
rocks:x:500:
clouds:x:501:
[5] 07:03:35 [SUCCESS] 10.1.1.104
rocks:x:500:
clouds:x:501:
```
