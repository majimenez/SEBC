<h1>List the cloud provider you are using (AWS, GCE, Azure, other)</h1>>
<pre>
eu-west-1c
ami-e4aefd97 with volumes resized to a 100Gb based on centos 6.5
centos 6.5
</pre>
<h1>List the Linux release you have chosen</h1>
<pre>
cat /etc/redhat-release 
CentOS release 6.5 (Final)
</pre>
<h1>Show that the disk space on each node is at least 30 GB</h1>
<pre>
for i in  `echo $NODES`; do ssh -i clouderaSEBC.pem $i echo $i; df -h ; done
172.31.37.252
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        99G  675M   93G   1% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
172.31.41.42
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        99G  675M   93G   1% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
172.31.33.96
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        99G  675M   93G   1% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
172.31.39.2
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        99G  675M   93G   1% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
172.31.32.90
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        99G  675M   93G   1% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
</pre>

<h1>List the command and output for yum repolist enabled</h1>
<pre>
yum repolist enabled
Loaded plugins: fastestmirror, presto
base                                                                                                          | 3.7 kB     00:00     
base/primary_db                                                                                               | 4.7 MB     00:00     
extras                                                                                                        | 3.4 kB     00:00     
extras/primary_db                                                                                             |  29 kB     00:00     
updates                                                                                                       | 3.4 kB     00:00     
updates/primary_db                                                                                            | 1.4 MB     00:00     
repo id                                                                           repo name                                                                                    status
base                                                                              CentOS-6 - Base                                                                              6,706
extras                                                                            CentOS-6 - Extras                                                                               45
updates                                                                           CentOS-6 - Updates                                                                             354
repolist: 7,105
</pre>

<h1>List the /etc/passwd entries for theresa and jeremy in your setup file</h1>
<pre>
root:x:0:
bin:x:1:bin,daemon
daemon:x:2:bin,daemon
sys:x:3:bin,adm
adm:x:4:adm,daemon
tty:x:5:
disk:x:6:
lp:x:7:daemon
mem:x:8:
kmem:x:9:
wheel:x:10:
mail:x:12:mail,postfix
uucp:x:14:
man:x:15:
games:x:20:
gopher:x:30:
video:x:39:
dip:x:40:
ftp:x:50:
lock:x:54:
audio:x:63:
nobody:x:99:
users:x:100:
floppy:x:19:
vcsa:x:69:
utmp:x:22:
utempter:x:35:
cdrom:x:11:
tape:x:33:
dialout:x:18:
saslauth:x:76:
postdrop:x:90:
postfix:x:89:
sshd:x:74:
labour:x:500:
conservative:x:501:
[root@ip-172-31-37-252 ~]# cat /etc/passwd
root:x:0:0:root:/root:/bin/bash
bin:x:1:1:bin:/bin:/sbin/nologin
daemon:x:2:2:daemon:/sbin:/sbin/nologin
adm:x:3:4:adm:/var/adm:/sbin/nologin
lp:x:4:7:lp:/var/spool/lpd:/sbin/nologin
sync:x:5:0:sync:/sbin:/bin/sync
shutdown:x:6:0:shutdown:/sbin:/sbin/shutdown
halt:x:7:0:halt:/sbin:/sbin/halt
mail:x:8:12:mail:/var/spool/mail:/sbin/nologin
uucp:x:10:14:uucp:/var/spool/uucp:/sbin/nologin
operator:x:11:0:operator:/root:/sbin/nologin
games:x:12:100:games:/usr/games:/sbin/nologin
gopher:x:13:30:gopher:/var/gopher:/sbin/nologin
ftp:x:14:50:FTP User:/var/ftp:/sbin/nologin
nobody:x:99:99:Nobody:/:/sbin/nologin
vcsa:x:69:69:virtual console memory owner:/dev:/sbin/nologin
saslauth:x:499:76:"Saslauthd user":/var/empty/saslauth:/sbin/nologin
postfix:x:89:89::/var/spool/postfix:/sbin/nologin
sshd:x:74:74:Privilege-separated SSH:/var/empty/sshd:/sbin/nologin
theresa:x:2000:501::/home/theresa:/bin/bash
jeremy:x:3000:500::/home/jeremy:/bin/bash
</pre>
```
Consider grep (theresa|jeremy) /etc/passwd
```
<h1>List the /etc/group entries for conservative and labour in your setup file</h1>
<pre>
root:x:0:
bin:x:1:bin,daemon
daemon:x:2:bin,daemon
sys:x:3:bin,adm
adm:x:4:adm,daemon
tty:x:5:
disk:x:6:
lp:x:7:daemon
mem:x:8:
kmem:x:9:
wheel:x:10:
mail:x:12:mail,postfix
uucp:x:14:
man:x:15:
games:x:20:
gopher:x:30:
video:x:39:
dip:x:40:
ftp:x:50:
lock:x:54:
audio:x:63:
nobody:x:99:
users:x:100:
floppy:x:19:
vcsa:x:69:
utmp:x:22:
utempter:x:35:
cdrom:x:11:
tape:x:33:
dialout:x:18:
saslauth:x:76:
postdrop:x:90:
postfix:x:89:
sshd:x:74:
labour:x:500:
conservative:x:501:
</pre>
```
Consider grep (labour|conservative) /etc/group
```


