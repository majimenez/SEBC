<b>The kinit command you use to authenticate your test user</b>
<pre>
[root@ip-172-31-2-87 ~]# kinit majimenez@MAJIMENEZ.ES
Password for majimenez@MAJIMENEZ.ES:
</pre>

<i>Password: T3mp0r@l</i>

<b>The output from a klist command listing your credentials and ticket lifetime</b>
<pre>
[root@ip-172-31-2-87 ~]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: majimenez@MAJIMENEZ.ES

Valid starting     Expires            Service principal
06/08/17 08:12:38  06/09/17 08:12:38  krbtgt/MAJIMENEZ.ES@MAJIMENEZ.ES
	renew until 06/15/17 08:12:38
</pre>