Tried to enable TLS but having issues in restarting cloudera manager.

Reverted the configuration of DB attribute 'agent_tls' and reverted to false.
Reverted config.ini config file for the cloudera-scm-agent and set use_tls=1


Creating new principal for `gioconte`:
 ```
Authenticating as principal admin/admin@MOVIRI.COM with password.
Password for admin/admin@MOVIRI.COM: 
kadmin:  add_principal gioconte
WARNING: no policy specified for gioconte@MOVIRI.COM; defaulting to no policy
Enter password for principal "gioconte@MOVIRI.COM": 
Re-enter password for principal "gioconte@MOVIRI.COM": 
Principal "gioconte@MOVIRI.COM" created.
kadmin:  exit
 ```
 
Authenticating new principal  `gioconte`:

 ```
[gioconte@ip-172-31-19-14 ~]$ kinit 
Password for gioconte@MOVIRI.COM: 
[gioconte@ip-172-31-19-14 ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_501
Default principal: gioconte@MOVIRI.COM

Valid starting     Expires            Service principal
11/16/16 15:40:19  11/17/16 15:40:19  krbtgt/MOVIRI.COM@MOVIRI.COM
	renew until 11/23/16 15:40:19
 ```
