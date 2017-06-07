<pre>
{
  "timestamp" : "2017-06-07T22:00:30.139Z",
  "clusters" : [ {
    "name" : "cluster",
    "displayName" : "majimenez",
    "version" : "CDH5",
    "fullVersion" : "5.8.3",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-3ed61aaa76499ae0c14ae5a9a0567574",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-00cd393201d6afaa8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6tugj79sorpawp5o0g3o8cc2l"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-731dd51c2295e1189bb36ada10eb29c9",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-040809a95c747957a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6g9nd006cgroxmesrndn8yku5"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-79ac08a554780aa0b41efb1bc6032ac4",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0a87e196d9c7f4d22"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "37zwo7sapq8pesiz8dq2moqc9"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      } ],
      "displayName" : "ZooKeeper",
      "roleConfigGroups" : [ {
        "name" : "zookeeper-SERVER-BASE",
        "displayName" : "Server Default Group",
        "roleType" : "SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "zookeeper"
        },
        "config" : {
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "867172352"
          } ]
        }
      } ]
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
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
        "name" : "oozie-OOZIE_SERVER-3ed61aaa76499ae0c14ae5a9a0567574",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-00cd393201d6afaa8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "epqkl04jcu0bs2l85zbde6xtc"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "oozie-OOZIE_SERVER-BASE"
        }
      } ],
      "displayName" : "Oozie",
      "roleConfigGroups" : [ {
        "name" : "oozie-OOZIE_SERVER-BASE",
        "displayName" : "Oozie Server Default Group",
        "roleType" : "OOZIE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "oozie"
        },
        "config" : {
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-2-87.eu-west-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "T3mp0r@l"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "867172352"
          } ]
        }
      } ]
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-2-87.eu-west-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "T3mp0r@l"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-3ed61aaa76499ae0c14ae5a9a0567574"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-3ed61aaa76499ae0c14ae5a9a0567574",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-00cd393201d6afaa8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4kvo2eb4nwm9c96hqjbsjlhde"
          }, {
            "name" : "secret_key",
            "value" : "2F8Jt7Vodmv2hjsOtGGkW905a1OIr3"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_SERVER-BASE"
        }
      } ],
      "displayName" : "Hue",
      "roleConfigGroups" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-BASE",
        "displayName" : "Balancer de carga Default Group",
        "roleType" : "HUE_LOAD_BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hue-HUE_SERVER-BASE",
        "displayName" : "Hue Server Default Group",
        "roleType" : "HUE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hue-KT_RENEWER-BASE",
        "displayName" : "Kerberos Ticket Renewer Default Group",
        "roleType" : "KT_RENEWER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "8XP2l3V25jehyE7ebjLvKNf1Y7Ap6c"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "XIVu7is3DgHGeL5bQfYx6XgQcjTnsa"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "157bkdR2tNjdjjcBWcuRczphnSSUuG"
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
        "name" : "hdfs-BALANCER-731dd51c2295e1189bb36ada10eb29c9",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-040809a95c747957a"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-BALANCER-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-79ac08a554780aa0b41efb1bc6032ac4",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0a87e196d9c7f4d22"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e28i5o1naxhcyuabdyvlfk4r3"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-1"
        }
      }, {
        "name" : "hdfs-DATANODE-e0cfb9e02c98d95e68551dbd55cc2503",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0d3fd95d15fc7c9a4"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "czs3ffkjzctr587kfkfbdfojx"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-ea6b69c6cba3652de64d0813ae3694fc",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0e9ba119cadfe4cc7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "jqbuda5g8eed8rym1z809x0m"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-731dd51c2295e1189bb36ada10eb29c9",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-040809a95c747957a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a9b8nelk1ib936xsssk2fk9pu"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-79ac08a554780aa0b41efb1bc6032ac4",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0a87e196d9c7f4d22"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2g9s3muj8m4un1ls8n9u70qfc"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-HTTPFS-3ed61aaa76499ae0c14ae5a9a0567574",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-00cd393201d6afaa8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2kqeoubzs2tmcdxvyac9zvdlx"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-HTTPFS-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-3ed61aaa76499ae0c14ae5a9a0567574",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-00cd393201d6afaa8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "69x1pqkilcbvah0mm8vdv75ts"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-731dd51c2295e1189bb36ada10eb29c9",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-040809a95c747957a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "645c8sego8bovb2iv4cb7sgd0"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-79ac08a554780aa0b41efb1bc6032ac4",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0a87e196d9c7f4d22"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6fn1hc51ksie9gi1tkyl2opho"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-731dd51c2295e1189bb36ada10eb29c9",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-040809a95c747957a"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "majimenezHA"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "majimenezHA"
          }, {
            "name" : "namenode_id",
            "value" : "42"
          }, {
            "name" : "role_jceks_password",
            "value" : "6ysdy39f18go5hkkz7pu09shs"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-79ac08a554780aa0b41efb1bc6032ac4",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0a87e196d9c7f4d22"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "majimenezHA"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "majimenezHA"
          }, {
            "name" : "namenode_id",
            "value" : "53"
          }, {
            "name" : "role_jceks_password",
            "value" : "89opf970laap9fqx7wndcwfy7"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      } ],
      "displayName" : "HDFS",
      "roleConfigGroups" : [ {
        "name" : "hdfs-BALANCER-BASE",
        "displayName" : "Balancer Default Group",
        "roleType" : "BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-1",
        "displayName" : "DataNode Group 1",
        "roleType" : "DATANODE",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3170683699"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-BASE",
        "displayName" : "DataNode Default Group",
        "roleType" : "DATANODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3170683699"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-BASE",
        "displayName" : "Failover Controller Default Group",
        "roleType" : "FAILOVERCONTROLLER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-BASE",
        "displayName" : "HttpFS Default Group",
        "roleType" : "HTTPFS",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-BASE",
        "displayName" : "JournalNode Default Group",
        "roleType" : "JOURNALNODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-BASE",
        "displayName" : "NameNode Default Group",
        "roleType" : "NAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "2154823680"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-BASE",
        "displayName" : "NFS Gateway Default Group",
        "roleType" : "NFSGATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-BASE",
        "displayName" : "SecondaryNameNode Default Group",
        "roleType" : "SECONDARYNAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "2154823680"
          } ]
        }
      } ],
      "replicationSchedules" : [ ],
      "snapshotPolicies" : [ ]
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
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
          "value" : "OGq5T4nLo5DMlB0DfpXffYHbl9zcb2"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-731dd51c2295e1189bb36ada10eb29c9",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-040809a95c747957a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4nkguam9kbf63lrbuw9gudt9t"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-JOBHISTORY-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-79ac08a554780aa0b41efb1bc6032ac4",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0a87e196d9c7f4d22"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5vhg3dqbikdt21orhkc6h73z0"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-1"
        }
      }, {
        "name" : "yarn-NODEMANAGER-e0cfb9e02c98d95e68551dbd55cc2503",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0d3fd95d15fc7c9a4"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1gmft0oyr0pyy2zd674d1d75b"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-ea6b69c6cba3652de64d0813ae3694fc",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0e9ba119cadfe4cc7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dq7wn868wvt5op39gestaewr0"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-731dd51c2295e1189bb36ada10eb29c9",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-040809a95c747957a"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "48"
          }, {
            "name" : "role_jceks_password",
            "value" : "exuhu7swjkdxvch2zaiecdoj8"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-RESOURCEMANAGER-BASE"
        }
      } ],
      "displayName" : "YARN (MR2 Included)",
      "roleConfigGroups" : [ {
        "name" : "yarn-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-BASE",
        "displayName" : "JobHistory Server Default Group",
        "roleType" : "JOBHISTORY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-1",
        "displayName" : "NodeManager Group 1",
        "roleType" : "NODEMANAGER",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
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
            "value" : "3072"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-BASE",
        "displayName" : "NodeManager Default Group",
        "roleType" : "NODEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          }, {
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
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "5250"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-BASE",
        "displayName" : "ResourceManager Default Group",
        "roleType" : "RESOURCEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5250"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        }
      } ]
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-2-87.eu-west-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "T3mp0r@l"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-3ed61aaa76499ae0c14ae5a9a0567574",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-00cd393201d6afaa8"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-HIVEMETASTORE-3ed61aaa76499ae0c14ae5a9a0567574",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-00cd393201d6afaa8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "anc7y2c29nx9gw0hn0x045hhw"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVEMETASTORE-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-3ed61aaa76499ae0c14ae5a9a0567574",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-00cd393201d6afaa8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "95dzd3n7asjl9b2zzr17cfxrm"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVESERVER2-BASE"
        }
      }, {
        "name" : "hive-WEBHCAT-3ed61aaa76499ae0c14ae5a9a0567574",
        "type" : "WEBHCAT",
        "hostRef" : {
          "hostId" : "i-00cd393201d6afaa8"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_webhcat_secret_key",
            "value" : "T3J24VQXDF4UT3FywRvSq6rBIx5s1e"
          }, {
            "name" : "role_jceks_password",
            "value" : "4yzb6756y0x7ikm3ap2jp6xgs"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-WEBHCAT-BASE"
        }
      } ],
      "displayName" : "Hive",
      "roleConfigGroups" : [ {
        "name" : "hive-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-BASE",
        "displayName" : "Hive Metastore Server Default Group",
        "roleType" : "HIVEMETASTORE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "867172352"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-BASE",
        "displayName" : "HiveServer2 Default Group",
        "roleType" : "HIVESERVER2",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "867172352"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2380634521"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "400"
          } ]
        }
      }, {
        "name" : "hive-WEBHCAT-BASE",
        "displayName" : "WebHCat Server Default Group",
        "roleType" : "WEBHCAT",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      } ],
      "replicationSchedules" : [ ]
    } ],
    "parcels" : [ {
      "product" : "CDH",
      "version" : "5.8.3-1.cdh5.8.3.p0.2",
      "stage" : "DISTRIBUTED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    }, {
      "product" : "CDH",
      "version" : "5.8.3-1.cdh5.8.3.p0.2",
      "stage" : "ACTIVATED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-040809a95c747957a",
    "ipAddress" : "172.31.0.201",
    "hostname" : "ip-172-31-0-201.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0d3fd95d15fc7c9a4",
    "ipAddress" : "172.31.10.156",
    "hostname" : "ip-172-31-10-156.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0a87e196d9c7f4d22",
    "ipAddress" : "172.31.14.238",
    "hostname" : "ip-172-31-14-238.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-00cd393201d6afaa8",
    "ipAddress" : "172.31.2.87",
    "hostname" : "ip-172-31-2-87.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0e9ba119cadfe4cc7",
    "ipAddress" : "172.31.4.48",
    "hostname" : "ip-172-31-4-48.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__0b935f88-632f-45dc-9304-22eb1aef705e",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "2b291fe233a34fb569654c092941653479d1d1b196123e9163540fa9966cfe0f",
    "pwSalt" : -4760004960156129375,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-3ed61aaa76499ae0c14ae5a9a0567574",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "da58616b45065a991b1c0078ad2d2981b0d3481c4c6ec0f6627d53468da2bc5a",
    "pwSalt" : 7847600207986774222,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-3ed61aaa76499ae0c14ae5a9a0567574",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "24b3dcba43de1e06905bbe92f9d4aeca004c8aa936d93b282d2888504d16bf44",
    "pwSalt" : -4406202795560815706,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-3ed61aaa76499ae0c14ae5a9a0567574",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "94102d45fbf51c08b9d674e39dfea4f0181e3f586e6674d2f9ffe6ea477d2010",
    "pwSalt" : 5301979612807945512,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-3ed61aaa76499ae0c14ae5a9a0567574",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "dfef86948f4345901d74c93c7f7c4ca5fe7a1ad5489da09e8cab8dc5f7b1b2f1",
    "pwSalt" : -3799794865824301681,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "25065bc447a15dde897be93f6c8bd6711f39411170ef91a32c0f006b0f2ec0a0",
    "pwSalt" : -7767927670650809807,
    "pwLogin" : true
  }, {
    "name" : "majimenez",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "427d59c914beb0b0bfa7cf6dcdc8ce291dcc023582d666a70eb6000aaa396ce0",
    "pwSalt" : -1928137410149268586,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "6118baa6f54fc6549de6e683d8cc41029063f72ad94e6a63da8a162a825fc1b5",
    "pwSalt" : -3611921322934445938,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.8.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20161019-1014",
    "gitHash" : "518f0d6d44abc87bc392646e4369a20c8192b7cf",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-3ed61aaa76499ae0c14ae5a9a0567574",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-00cd393201d6afaa8"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2tr8tbwmo2k2jjj9ud73gyb2i"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ALERTPUBLISHER-BASE"
      }
    }, {
      "name" : "mgmt-EVENTSERVER-3ed61aaa76499ae0c14ae5a9a0567574",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-00cd393201d6afaa8"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "97odt47ou4x47jie48yfb1159"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-EVENTSERVER-BASE"
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-3ed61aaa76499ae0c14ae5a9a0567574",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-00cd393201d6afaa8"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5wj0c1se5ke3tllye5ji9sii2"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-HOSTMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-3ed61aaa76499ae0c14ae5a9a0567574",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-00cd393201d6afaa8"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2yq1v0riiy93trg0i20o89kw1"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-REPORTSMANAGER-BASE"
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-3ed61aaa76499ae0c14ae5a9a0567574",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-00cd393201d6afaa8"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "eoz3nzuf8thlx8v0g6cm93nuw"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-SERVICEMONITOR-BASE"
      }
    } ],
    "displayName" : "Cloudera Management Service",
    "roleConfigGroups" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-BASE",
      "displayName" : "Activity Monitor Default Group",
      "roleType" : "ACTIVITYMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-BASE",
      "displayName" : "Alert Publisher Default Group",
      "roleType" : "ALERTPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-BASE",
      "displayName" : "Event Server Default Group",
      "roleType" : "EVENTSERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "867172352"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-BASE",
      "displayName" : "Host Monitor Default Group",
      "roleType" : "HOSTMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "867172352"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1127219200"
        }, {
          "name" : "firehose_storage_dir",
          "value" : "/var/log/cloudera-host-monitor"
        } ]
      }
    }, {
      "name" : "mgmt-NAVIGATOR-BASE",
      "displayName" : "Navigator Audit Server Default Group",
      "roleType" : "NAVIGATOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-NAVIGATORMETASERVER-BASE",
      "displayName" : "Navigator Metadata Server Default Group",
      "roleType" : "NAVIGATORMETASERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-BASE",
      "displayName" : "Reports Manager Default Group",
      "roleType" : "REPORTSMANAGER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-2-87.eu-west-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "T3mp0r@l"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "867172352"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-BASE",
      "displayName" : "Service Monitor Default Group",
      "roleType" : "SERVICEMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "867172352"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1127219200"
        }, {
          "name" : "firehose_storage_dir",
          "value" : "/var/log/cloudera-service-monitor"
        } ]
      }
    } ]
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/28/2012 1:30"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/5.8.3/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  },
  "allHostsConfig" : {
    "items" : [ {
      "name" : "rm_enabled",
      "value" : "true"
    } ]
  },
  "peers" : [ {
    "name" : "ainowy",
    "type" : "REPLICATION",
    "url" : "http://ec2-34-249-47-205.eu-west-1.compute.amazonaws.com:7180",
    "username" : "__cloudera_internal_user__f3f7c71f-532d-479a-902d-89974e05e18d",
    "password" : "9ae2fcf1-8372-4992-a5f2-1a66826c464199fbd1b3-c24e-415e-9e2f-e0ad02f4d8df",
    "clouderaManagerCreatedUser" : true
  } ],
  "hostTemplates" : {
    "items" : [ ]
  }
}
</pre>