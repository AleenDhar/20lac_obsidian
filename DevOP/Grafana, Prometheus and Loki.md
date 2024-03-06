
#### 1. Prometheus Server


- Create a `prometheus-config.yml` file and copy the following configration. Don't forget to replace `<NDOEJS_SERVER_ADDRESS>` with actual value.

```yaml
global:
  scrape_interval: 4s

scrape_configs:
  - job_name: prometheus
    static_configs:
      - targets: ["<NDOEJS_SERVER_ADDRESS>"]
```

- Start the Prometheus Server using docker compose

```yaml
version: "3"

services:
  prom-server:
    image: prom/prometheus
    ports:
      - 9090:9090
    volumes:
      - ./prometheus.yml:/etc/prometheus/prometheus.yml
```

Great, The prometheus server is now up and running at PORT 9090

#### 2. Setup Grafana


```shell
docker run -d -p 3000:3000 --name=grafana grafana/grafana-oss
```

[![grafana](https://camo.githubusercontent.com/600daa5516ce791bb3162595c4a41013e3b1ed7ed7eed18051cebfb7d6eb15fc/68747470733a2f2f67726166616e612e636f6d2f7374617469632f696d672f67726166616e612f73686f77636173655f76697375616c697a652e6a7067)](https://camo.githubusercontent.com/600daa5516ce791bb3162595c4a41013e3b1ed7ed7eed18051cebfb7d6eb15fc/68747470733a2f2f67726166616e612e636f6d2f7374617469632f696d672f67726166616e612f73686f77636173655f76697375616c697a652e6a7067)

### 3. Setup Loki Server


```shell
docker run -d --name=loki -p 3100:3100 grafana/loki
```