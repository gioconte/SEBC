Tried to enable TLS but having issues in restarting cloudera manager. It was basically checking for the certificate that was not created.

Reverted the configuration of DB attribute `agent_tls` ans set to `false`.
Reverted `config.ini` file for the cloudera-scm-agent and set `use_tls=0`
