---
title: "Grafana + ex"
date: 2022-03-07T14:31:39+09:00
draft: false
---

## セットアップ編
### InfluxDB
```bash
sudo apt update | sudo apt install influxdb -y
```

### Grafana
導入手順: https://grafana.com/docs/grafana/latest/installation/debian/
```bash
echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
sudo apt update | sudo apt install grafana -y
```
