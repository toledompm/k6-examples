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

### Querying data:
An instance of [chronograf](https://www.influxdata.com/time-series-platform/chronograf/) is included in the `docker-compose` file. It can be accessed [here](http:localhost:8888). The default DB name is `k6`.

### Sources:
- [InfluxDB options](https://k6.io/docs/results-visualization/influxdb-+-grafana/#influxdb-options)
