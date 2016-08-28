# spark-sample

## Setup

**Software Versions**

* Spark 2.0.0
* Hadoop 2.7.2
* Java 1.8.0_92

**Steps**

1. Clone, and set up cluster (standalone type) of one master & one worker:

```bash
git clone https://github.com/gettyimages/docker-spark.git
cd docker-spark/

docker-compose up
```

Master Ports:

* 4040: Web UI - all other cluster managers
* 6066
* 7001-7006: See conf/master/spark-defaults.conf
* 7077: Spark Master Port (to submit jobs)
* 8080: Web UI (http://localhost:8080/) - standalone mode only

Worker Ports:

* 7012-7016: See conf/worker/spark-defaults.conf
* 8081: Web UI (http://localhost:8081/) - standalone mode only
* 8881: Spark Worker Port



