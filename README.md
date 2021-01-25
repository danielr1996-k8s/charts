# My [Helm](https://helm.sh) Charts

This repository contains [Helm](https://helm.sh) charts for various projects

* [echo-server](charts/echo/)
* [instrumented-app](charts/instrumented-app)
* [prometheus-operator](charts/prometheus-operator)
* [prometheus](charts/prometheus)

## Installing Charts from this Repository

``` shell
helm repo add danielr1996 https://danielr1996-k8s.github.io/charts
helm install danielr1996/<chart-name>
```
