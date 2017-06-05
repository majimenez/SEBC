
<b>1. Check vm.swappiness on all your nodes</b>

[centos@ip-172-31-39-206 ~]$ cat /proc/sys/vm/swappiness <br/>
1 <br/>
<br/>
[root@ip-172-31-39-206 centos]# cat /etc/sysctl.conf | grep swap<br/>
vm.swappiness = 1<br/>
<br/>

<b>2. Show the mount attributes of all volumes</b>

<pre>
[root@ip-172-31-39-206 centos]# cat /etc/fstab 

#
# /etc/fstab
# Created by anaconda on Mon Feb 22 16:51:19 2016
#
# Accessible filesystems, by reference, are maintained under '/dev/disk'
# See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info
#
UUID=cdbab22a-45d6-4cce-95a3-681f42187a46 /                       ext4    defaults        1 1
tmpfs                   /dev/shm                tmpfs   defaults        0 0
devpts                  /dev/pts                devpts  gid=5,mode=620  0 0
sysfs                   /sys                    sysfs   defaults        0 0
proc                    /proc                   proc    defaults        0 0
</pre>

<pre>
[root@ip-172-31-39-206 centos]# lsblk 
NAME    MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  30G  0 disk 
└─xvda1 202:1    0   8G  0 part /
xvdb    202:16   0  30G  0 disk 
</pre>

<b>3. Show the reserve space of any non-root, ext-based volumes
- XFS volumes do not maintain reserve space</b>

<pre>
I don't have such volumes in my nodes.
</pre>


<b>4. Disable transparent hugepage support</b>

<pre>
[root@ip-172-31-39-206 centos]# cat /sys/kernel/mm/redhat_transparent_hugepage/enabled
always madvise [never]
[root@ip-172-31-39-206 centos]# cat /sys/kernel/mm/redhat_transparent_hugepage/defrag
always madvise [never]
</pre>

<b>5. List your network interface configuration</b>
<pre>
[root@ip-172-31-39-206 centos]# ifconfig -a
eth0      Link encap:Ethernet  HWaddr 0A:5F:E9:07:51:E7  
          inet addr:172.31.39.206  Bcast:172.31.47.255  Mask:255.255.240.0
          inet6 addr: fe80::85f:e9ff:fe07:51e7/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:419 errors:0 dropped:0 overruns:0 frame:0
          TX packets:395 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000 
          RX bytes:42516 (41.5 KiB)  TX bytes:47437 (46.3 KiB)
          Interrupt:144 

lo        Link encap:Local Loopback  
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0 
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)
</pre>

<b>6. List forward and reverse host lookups using getent or nslookup</b>

<pre>

[root@ip-172-31-39-206 centos]# nslookup ip-172-31-39-206
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
Name:	ip-172-31-39-206.us-east-2.compute.internal
Address: 172.31.39.206

</pre>

<b>7. Show the nscd service is running</b>

<pre>
[root@ip-172-31-39-206 centos]# service nscd status
nscd (pid 1417) is running...
</pre>

<b>8. Show the ntpd service is running</b>

<pre>
[root@ip-172-31-39-206 centos]# service ntpd status
ntpd (pid  1515) is running...
</pre>