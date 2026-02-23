# Texera Observability Stack

This repo deploys **Grafana**, **Loki**, and an **OpenTelemetry Collector** for Apache/Texera logging on Kubernetes.

## Install

1. Clone the repo:
```bash
git clone https://github.com/Ma77Ball/Texera_Observability_Stack.git
cd Texera_Observability_Stack
```

2. Install with Helm (example release name: texera):
```bash
helm install texera . --namespace texera-observability --create-namespace
```

3. Verify:
```bash
kubectl get pods -n texera-observability
kubectl get svc -n texera-observability
View Grafana (port 3000)
```

4. Port-forward Grafana:

```bash
kubectl -n texera-observability port-forward svc/grafana 3000:3000
```

5. Open:

[http://localhost:3000](http://localhost:3000)
