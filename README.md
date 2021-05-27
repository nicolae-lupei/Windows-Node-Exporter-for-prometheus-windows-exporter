# Windows-Node-Exporter-for-prometheus-windows-exporter

Uses metrics from [windows_exporter](https://github.com/prometheus-community/windows_exporter)

Link on grafana dashboards with id: [14499](https://grafana.com/grafana/dashboards/14499)

Features:

- Node selector
- Summary CPU load
- Memory stats
- Network load
- Hard disks usage
- Service state summary
Prometheus config:
```yml
- job_name: 'win-exporter'
    static_configs:
      - targets: ['192.168.0.1:9182']
```
`192.168.0.1` - Windows node where windows_exporter is installed

Use `['192.168.0.1:9182', '192.168.0.2:9182']` for multiple hosts

Install windows-exporter with [choco](https://community.chocolatey.org/packages/prometheus-windows-exporter.install)
