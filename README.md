# My [Helm](https://helm.sh) Charts

This repository contains [Helm](https://helm.sh) charts for various projects

* [echo-server](charts/echo/)

## Installing Charts from this Repository

Add the Repository to Helm:

    helm repo add my-charts https://danielr1996-k8s.github.io/charts

Install echo-server:

    helm install my-charts/echo


kubectl create namespace kube-ops
kubectl label namespace default monitor=true
helm upgrade --install prom-operator charts/prometheus-operator/ --namespace kube-ops
helm upgrade --install prom-stack charts/prometheus-stack/ --namespace kube-ops
helm upgrade --install app charts/instrumented-app/

kubectl port-forward service/prometheus-operated -n kube-ops 80:9090