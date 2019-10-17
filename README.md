# multi-k8s

Kubernetes Example With Multiple Services (React, Express, Worker)

## Requirements

- Kubernetes
- minikube >= 1.3.1
- kubectl >= 1.15.0

## Version

1.0.0

## Installation

Download zip file and extract it [latest pre-built release](https://github.com/reysmerwvr/multi-k8s). Or clone the repository and cd into it.

This project uses a number of open source projects to work properly:

- [Kubernetes] - Production-Grade Container Orchestration

## Setup

Install kubectl and minikube for your OS.

[macOS](https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl-on-macos)
[Windows](https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl-on-windows)
[Linux](https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl-on-linux)

## Run minikube

```bash
hyperv
$ minikube start --vm-driver hyperv --hyperv-virtual-switch "<Minikube Name>"
virtualbox
minikube start –vm-driver=virtualbox -p <name>
```

Once running minikube

```bash
cd multi-k8s
minikube status
kubectl cluster-info
Generate your secrets
kubectl create secret generic pgpassword --from-literal PG_PASSWORD=yourpass
kubectl apply -f k8s
```

To verify pods/deployments/persistent volumes/persistent volume claims/services status

```bash
cd multi-k8s
kubectl get deployments
kubectl get services
kubectl get storageclass
kubectl get pv
kubectl get pvc
```

To verify minikube ip/dashboard

```bash
cd multi-k8s/k8s
minikube ip
minikube dashboard
```

### Todos

- Add code comments

[//]: # "These are reference links used in the body of this note and get stripped out when the markdown processor does
its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax"
[Kubernetes]: https://kubernetes.io/
