# lab

## iperf.yml

```bash
sudo dnf install iperf3
iperf3 -c 127.0.0.1
```

## monitoring.yml

- `localhost:3000` -> `admin/admin`
- `Data sources` -> `Add data source` -> `Prometheus (http://prometheus:9090)`
- `Dashboards` -> `Import dashboard` -> `ID: 1860` -> `Node Exporter Full`
