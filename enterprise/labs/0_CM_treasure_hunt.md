1. What is ubertask optimization?
Ubertasks optimization runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.
2. Where in CM is the Kerberos Security Realm value displayed?
The Kerberos Security Realm value is displayed here:
`Administration -> Settings -> Kerberos -> Kerberos Security Realm`
3. Which CDH service(s) host a property for enabling Kerberos authentication?

4. How do you upgrade the CM agents?
You need first to upgrade the cloudera manager Server. Once the CM server is upgrade and restarted a wizard pops up to upgrade the cloudera manager agents and optionally the JDK

5. Give the tsquery statement used to chart Hue's CPU utilization?

6. Name all the roles that make up the Hive service
  - Hive Server2
  - Hive Metastore Server
  - WebHcat Server
  - Hive Gateway (just configuration flies for the clients, no active role)

7. What steps must be completed before integrating Cloudera Manager with Kerberos?
