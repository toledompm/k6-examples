## K6 InfluxDB test

Simple example, saving k6 results in InfluxDB.

### Requirements:
- docker + docker-compose || Access to a InfluxDB instance
- k6

### Usage:

Docker
``` bash
$ docker-compose up -d
$ make run
```

Non docker
``` bash
$ k6 run --out influxdb=<INFLUX_DB_ENDPOINT> index.js
```

### Sources:
- [InfluxDB options](https://k6.io/docs/results-visualization/influxdb-+-grafana/#influxdb-options)
