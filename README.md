# My [Helm](https://helm.sh) Charts

This repository contains [Helm](https://helm.sh) charts for various projects

* [echo-server](charts/echo/)

## Installing Charts from this Repository

Add the Repository to Helm:

    helm repo add my-charts https://danielr1996-k8s.github.io/charts

Install echo-server:

    helm install my-charts/echo