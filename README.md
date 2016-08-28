# spark-sample

## Setup

**Software Versions**

* Spark 2.0.0
* Hadoop 2.7.2
* Java 1.8.0_92

**Steps**

1. Clone, and set up cluster (standalone type) of one master & one worker (2 cores, 1024.0 MB RAM):

```bash
git clone https://github.com/gettyimages/docker-spark.git
cd docker-spark/

docker-compose up
```

2. Should see log outputs like

```
Started daemon with process name: 1@master
...
Successfully started service 'sparkMaster' on port 7077.
...
Starting Spark master at spark://master:7077
...
Successfully started service 'MasterUI' on port 8080.
...
Successfully started service on port 6066.
...
Started REST server for submitting applications on port 6066
...
I have been elected leader! New state: ALIVE
...
Registering worker 172.17.0.4:8881 with 2 cores, 1024.0 MB RAM
```

and 

```
Started daemon with process name: 1@worker
...
Successfully started service 'sparkWorker' on port 8881.
...
Starting Spark worker 172.17.0.4:8881 with 2 cores, 1024.0 MB RAM
...
Successfully started service 'WorkerUI' on port 8081.
...
Successfully registered with master spark://master:7077
```

Master Ports:

* 4040: Web UI - all other cluster managers
* 6066: Spark Master Port (to submit jobs, cluster-mode)
* 7001-7006: See conf/master/spark-defaults.conf
* 7077: Spark Master Port (to submit jobs, client-mode)
* 8080: Web UI (http://localhost:8080/) - standalone mode only

Worker Ports:

* 7012-7016: See conf/worker/spark-defaults.conf
* 8081: Web UI (http://localhost:8081/) - standalone mode only
* 8881: Spark Worker Port



