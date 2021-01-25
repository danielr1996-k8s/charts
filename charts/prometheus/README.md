# Prometheus
Deploy a prometheus instance using [prometheus-operator](https://github.com/prometheus-operator/prometheus-operator)

Contains the following (Custom) Resources
- Prometheus
- ClusterRole and ClusterRoleBinding
- ServiceAccount

To add a target to be monitored by prometheus install a ServiceMonitor
```yaml
apiVersion: monitoring.coreos.com/v1
kind: ServiceMonitor
metadata:
  name: prometheus-servicemonitor
  namespace: {{ .Release.Namespace }}
  labels:
    monitor: "true" # Needed to be selected by the prometheus instance
spec:
  selector:
    matchLabels:
      app: example-app # Needed to select the Service to be monitored
  endpoints:
    - port: web # Endpoint name of the Service
```