Tried to enable TLS but having issues in restarting cloudera manager. It was basically checking for the certificate that was not created.

Reverted the configuration of DB attribute `agent_tls` ans set to `false`.
Reverted `config.ini` file for the cloudera-scm-agent and set `use_tls=0`


Got the tls run with the following commands:

```
keytool -genkeypair -keystore example.keystore -keyalg RSA -alias ip-172-31-22-224 \
-dname "CN=ip-172-31-22-224.eu-central-1.compute.internal,OU=Security,O=Example,L=Denver,ST=Colorado,C=US" -storepass giorgione -keypass giorgione

sudo cp $JAVA_HOME/jre/lib/security/cacerts $JAVA_HOME/jre/lib/security/jssecacerts

keytool -export -alias ip-172-31-22-224 -keystore example.keystore -rfc -file selfsigned.cer

cp selfsigned.cer /opt/cloudera/security/x509/ip-172-31-22-224.pem

keytool -import -alias ip-172-31-22-224 -file /opt/cloudera/security/jks/selfsigned.cer -keystore /usr/java/jdk1.8.0_102/jre/lib/security/jssecacerts -storepass changeit

mv /opt/cloudera/security/jks/example.keystore /opt/cloudera/security/jks/cmhost-keystore.jks

```

Set TLS path file to keystore and set the password in CM.

Restart cloudera manager

Than enable TLS Encryption in CM.

Restart both cloudera manager server and cloudera manager agents on all hosts!

