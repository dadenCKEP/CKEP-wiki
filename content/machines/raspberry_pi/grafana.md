---
title: "Grafana + ex"
date: 2022-03-07T14:31:39+09:00
draft: false
---

## セットアップ編
### InfluxDB
導入手順: https://portal.influxdata.com/downloads/
```bash
wget -qO- https://repos.influxdata.com/influxdb.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/influxdb.gpg > /dev/null
export DISTRIB_ID=$(lsb_release -si); export DISTRIB_CODENAME=$(lsb_release -sc)
echo "deb [signed-by=/etc/apt/trusted.gpg.d/influxdb.gpg] https://repos.influxdata.com/${DISTRIB_ID,,} ${DISTRIB_CODENAME} stable" | sudo tee /etc/apt/sources.list.d/influxdb.list > /dev/null

sudo apt-get update && sudo apt-get install influxdb2
```
手順2: https://docs.influxdata.com/influxdb/v2.1/tools/grafana/

### Grafana
導入手順: https://grafana.com/docs/grafana/latest/installation/debian/
```bash
echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
sudo apt update | sudo apt install grafana -y
```
手順2: https://grafana.com/docs/grafana/latest/getting-started/getting-started-influxdb/
