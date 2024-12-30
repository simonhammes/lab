# lab

## forgejo.yml

### Instructions
- `127.0.0.1:8002` -> use default settings + create admin user
- Generate Forgejo/Gitea token (scopes: `repository` (read/write), `user` (read)) -> `GITEA_TOKEN`
- Generate GitHub token (scopes: `Contents` (read-only), `Metadata` (read-only)) -> `GITHUB_TOKEN`

## iperf.yml

```bash
sudo dnf install iperf3
iperf3 -c 127.0.0.1
```

## monitoring.yml

```bash
# Source: https://stackoverflow.com/questions/50009065/how-to-persist-data-in-prometheus-running-in-a-docker-container#comment116094474_50009322
mkdir -p volumes/prometheus
sudo chown 65534:65534 volumes/prometheus

mkdir -p volumes/grafana
sudo chown 472:0 volumes/grafana
```

### Dashboards
- `localhost:3000` -> `admin/admin`
- `Data sources` -> `Add data source` -> `Prometheus (http://prometheus:9090)`
- `Dashboards` -> `Import dashboard` -> `ID: 1860` -> `Node Exporter Full`
