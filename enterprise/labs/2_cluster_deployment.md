Here the output of `curl -u admin:admin 'http://54.93.218.251:7180/api/v2/cm/deployment'`


```
{
  "timestamp" : "2016-11-16T10:16:27.613Z",
  "clusters" : [ {
    "name" : "gioconte",
    "version" : "CDH5",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-013d97f2d98bf346a2bdbcc02ffa7621",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-25370799"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1if8l3lhg7wr3dcgpaav29dm7"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-935303bf32c461a697abbb1973702382",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-2237079e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4o0hqz4y81d25zsyrdqd8jmke"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-a42b902095fc30c3a421bb27ddd00ca5",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-5e3707e2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9xmdnicrop9u637u8zl9pqs6a"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "7384732876"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "1781530624"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "1781530624"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "JpVVEn4UkICFAmooZ1yQgXPvzLTCyf"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "RSVuO79AzHydQX4fEt64Q1jMw3Q7Gt"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "8iajRgMTE76NWjTnM0onPOh6kxCPS4"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-a42b902095fc30c3a421bb27ddd00ca5",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-5e3707e2"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-013d97f2d98bf346a2bdbcc02ffa7621",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-25370799"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e7m4mcb0ttrmvblv1buzo1lbf"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-78b5d62e55a89d3e02c468e6f3d37918",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-2737079b"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4mt7u8zjjv2srea1d9n6mcvh5"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-935303bf32c461a697abbb1973702382",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-2237079e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4cmrlz83y8z2nu3pokzi41loz"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-935303bf32c461a697abbb1973702382",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-2237079e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "99j588aihksq2l9dx5ac6n589"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-a42b902095fc30c3a421bb27ddd00ca5",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-5e3707e2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cu4w032xnz3yczq1y4l5hknii"
          } ]
        }
      }, {
        "name" : "hdfs-GATEWAY-0131ba9c9fabe12915fc61806304782d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-9f350523"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-HTTPFS-935303bf32c461a697abbb1973702382",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-2237079e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "aq0nbw4gnewhnpf4d5wfyqgw"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-013d97f2d98bf346a2bdbcc02ffa7621",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-25370799"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ema2bk089zhpdkdzvf1d4qp3q"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-935303bf32c461a697abbb1973702382",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-2237079e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a6wjbubrjmhdagxkrerr3qblz"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-a42b902095fc30c3a421bb27ddd00ca5",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-5e3707e2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7lwyfqquipe1wo8hpktsoljlf"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-935303bf32c461a697abbb1973702382",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-2237079e"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "67"
          }, {
            "name" : "role_jceks_password",
            "value" : "6cwhjv227iwhy0go44x8tuoca"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-a42b902095fc30c3a421bb27ddd00ca5",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-5e3707e2"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "45"
          }, {
            "name" : "role_jceks_password",
            "value" : "105vqi2tfg4wzxath6o1pgy2q"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "4"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "5192"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5192"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "mQQs9ITas86TLdrXTYpjhnkHiESPfK"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-GATEWAY-0131ba9c9fabe12915fc61806304782d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-9f350523"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-a42b902095fc30c3a421bb27ddd00ca5",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-5e3707e2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3l0608iufkfx2kdqrql6uoy9"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-013d97f2d98bf346a2bdbcc02ffa7621",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-25370799"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "el9f3vvfc8qqkbxxto3zn13w9"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-78b5d62e55a89d3e02c468e6f3d37918",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-2737079b"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "eizeag002iw985jozh03eeg0"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-935303bf32c461a697abbb1973702382",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-2237079e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4qzu4s91n35bzihcydlft66cl"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-935303bf32c461a697abbb1973702382",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-2237079e"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "51"
          }, {
            "name" : "role_jceks_password",
            "value" : "38upn6kaknifsjmpc7cpugaov"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "2139095040"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "213909504"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "2139095040"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "1967967436"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "331"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-22-224.eu-central-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "password"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-0131ba9c9fabe12915fc61806304782d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-9f350523"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-013d97f2d98bf346a2bdbcc02ffa7621",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-25370799"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-78b5d62e55a89d3e02c468e6f3d37918",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-2737079b"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-935303bf32c461a697abbb1973702382",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-2237079e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-a42b902095fc30c3a421bb27ddd00ca5",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-5e3707e2"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-a42b902095fc30c3a421bb27ddd00ca5",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-5e3707e2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4073cmi7smumblda7q0nbnhno"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-a42b902095fc30c3a421bb27ddd00ca5",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-5e3707e2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9mggdx56uyug6zmq3zkd0viqb"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-22-224.eu-central-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "password"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-0131ba9c9fabe12915fc61806304782d",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-9f350523"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2wpwo8w77l9tqruokcaanjk0a"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-22-224.eu-central-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "password"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-935303bf32c461a697abbb1973702382"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-0131ba9c9fabe12915fc61806304782d",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-9f350523"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3ve2rinvytzwre5awn59726fk"
          }, {
            "name" : "secret_key",
            "value" : "cK97aMcHKvZVhzdbzNxAbzOlEIJagB"
          } ]
        }
      } ],
      "displayName" : "Hue"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-5e3707e2",
    "ipAddress" : "172.31.19.14",
    "hostname" : "ip-172-31-19-14.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-9f350523",
    "ipAddress" : "172.31.22.224",
    "hostname" : "ip-172-31-22-224.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-2237079e",
    "ipAddress" : "172.31.24.245",
    "hostname" : "ip-172-31-24-245.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-25370799",
    "ipAddress" : "172.31.24.246",
    "hostname" : "ip-172-31-24-246.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-2737079b",
    "ipAddress" : "172.31.24.248",
    "hostname" : "ip-172-31-24-248.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-0131ba9c9fabe12915fc61806304782d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "06e0a67f4a628b44f817c83d81b74a8fe7a19533e9fcbbb0c5b72f95c1efa520",
    "pwSalt" : -3848560769506885177,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-0131ba9c9fabe12915fc61806304782d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "84d4422bdfd3f6574d271cfb9edf2f56a5ea27b585d8faad091feb02b54bbfea",
    "pwSalt" : -4832886412755931384,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-0131ba9c9fabe12915fc61806304782d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "c15c45ef6948d900d6c6c26cbe17cee4cbdd8fd6af28ca6850698c65b5f12775",
    "pwSalt" : 7569929133062120050,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-0131ba9c9fabe12915fc61806304782d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "32add9d724ecf43bb19b6325cbaae14bc8cd10232f21eec95590004b03f604fa",
    "pwSalt" : -8712385941083615494,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-0131ba9c9fabe12915fc61806304782d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "a0bb9af6c7fa8c011d13084f72ad92f1f4ce993878bcd8e5a41c50d57ff33928",
    "pwSalt" : -8604792683559982066,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "6a4c209cfde2032d8219e1ff295c209732dfb441073cdb1cea34419df1d18048",
    "pwSalt" : -7591960661237962539,
    "pwLogin" : true
  }, {
    "name" : "gioconte",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "411ced9d850e9219eb8015f489c869449ddae14762d534ea5debd89fd7de1d41",
    "pwSalt" : 8619700649914139080,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "cc29092d2f2262cdc545c1cb40009774be28873d505a9a3e2e52ea2794b79a71",
    "pwSalt" : 108370759175788682,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.9.0",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20161006-1801",
    "gitHash" : "898a5e032c080e18833dfc58180761f6ef2ea351",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "ACTIVITYMONITOR",
        "items" : [ {
          "name" : "firehose_database_host",
          "value" : "ip-172-31-22-224.eu-central-1.compute.internal"
        }, {
          "name" : "firehose_database_name",
          "value" : "amon"
        }, {
          "name" : "firehose_database_password",
          "value" : "password"
        }, {
          "name" : "firehose_database_user",
          "value" : "amon"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-22-224.eu-central-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "password"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-0131ba9c9fabe12915fc61806304782d",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "i-9f350523"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "aaz4cax85o5spy6nlpnnf5he5"
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-0131ba9c9fabe12915fc61806304782d",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-9f350523"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "cf92yh6iqkeyn3rwt6yfdxs30"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-0131ba9c9fabe12915fc61806304782d",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-9f350523"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "cl4sacezq5l188p20issnewgd"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-0131ba9c9fabe12915fc61806304782d",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-9f350523"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "8wvlplbgyen3b745xvgezpd74"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-0131ba9c9fabe12915fc61806304782d",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-9f350523"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "61g10b0sgz4d7umky061ap207"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-0131ba9c9fabe12915fc61806304782d",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-9f350523"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "20qjh841bmzn31ze8o2httll3"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/25/2012 19:40"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/5.8.2/,https://archive.cloudera.com/cdh4/parcels/5.8.2/,https://archive.cloudera.com/impala/parcels/5.8.2/,https://archive.cloudera.com/search/parcels/5.8.2/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/5.8.2/,https://archive.cloudera.com/kafka/parcels/5.8.2/,https://archive.cloudera.com/navigator-keytrustee5/parcels/5.8.2/,https://archive.cloudera.com/spark/parcels/5.8.2/,https://archive.cloudera.com/sqoop-connectors/parcels/5.8.2/"
    } ]
  }
}```
