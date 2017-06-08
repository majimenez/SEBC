
<b>1. Check vm.swappiness on all your nodes</b>

[root@ip-172-31-2-87 ~]# cat /proc/sys/vm/swappiness<br/>
1<br/>
<br/>
root@ip-172-31-2-87 ~]# cat /etc/sysctl.conf | grep swap <br/>
vm.swappiness = 1<br/>
<br/>

<b>2. Show the mount attributes of all volumes</b>

<pre>
[root@ip-172-31-2-87 ~]# cat /etc/fstab 
LABEL=centos_root		/        ext4      defaults         0 0
devpts     /dev/pts  devpts  gid=5,mode=620   0 0
tmpfs      /dev/shm  tmpfs   defaults         0 0
proc       /proc     proc    defaults         0 0
sysfs      /sys      sysfs   defaults         0 0
</pre>

<pre>
root@ip-172-31-2-87 ~]# lsblk 
NAME MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
xvde 202:64   0  30G  0 disk /
</pre>

<b>3. Show the reserve space of any non-root, ext-based volumes
- XFS volumes do not maintain reserve space</b>

<pre>
I don't have such volumes in my nodes.
</pre>


<b>4. Disable transparent hugepage support</b>

<pre>
[root@ip-172-31-2-87 ~]# cat /sys/kernel/mm/redhat_transparent_hugepage/enabled
cat: /sys/kernel/mm/redhat_transparent_hugepage/enabled: No such file or directory
[root@ip-172-31-2-87 ~]# cat /sys/kernel/mm/redhat_transparent_hugepage/defrag
cat: /sys/kernel/mm/redhat_transparent_hugepage/defrag: No such file or directory
</pre>




<b>5. List your network interface configuration</b>
<pre>
root@ip-172-31-2-87 ~]# ifconfig -a
eth0      Link encap:Ethernet  HWaddr 02:98:61:A8:23:EE  
          inet addr:172.31.2.87  Bcast:172.31.15.255  Mask:255.255.240.0
          inet6 addr: fe80::98:61ff:fea8:23ee/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:2206185 errors:0 dropped:0 overruns:0 frame:0
          TX packets:1789553 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000 
          RX bytes:2690489329 (2.5 GiB)  TX bytes:3310389751 (3.0 GiB)
          Interrupt:24 

lo        Link encap:Local Loopback  
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:16436  Metric:1
          RX packets:1710827 errors:0 dropped:0 overruns:0 frame:0
          TX packets:1710827 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0 
          RX bytes:3164779724 (2.9 GiB)  TX bytes:3164779724 (2.9 GiB)
</pre>

<b>6. List forward and reverse host lookups using getent or nslookup</b>

<pre>

[root@ip-172-31-2-87 ~]# nslookup ip-172-31-2-87
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
Name:	ip-172-31-2-87.eu-west-1.compute.internal
Address: 172.31.2.87

</pre>

<b>7. Show the nscd service is running</b>

<pre>
[root@ip-172-31-2-87 ~]# service nscd status
nscd (pid 1045) is running...
</pre>

<b>8. Show the ntpd service is running</b>

<pre>
[root@ip-172-31-2-87 ~]# service ntpd status
ntpd (pid  1016) is running...
</pre>
