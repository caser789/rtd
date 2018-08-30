minikube
==============================

## setup minikube cluster

```
export KUBECONFIG=/Users/Jiao/xuejiao/docs/rtd_mkdocs_demo/kubeconfig
minikube start

minikube start --cpus=4 --memory=4000 --kubernetes-version=v1.7.2
```

## debug

```
minikube ssh
minikube ip
minikube dashboard
```

## 初始化 docker 环境

```
eval $(minikube docker-env)
```

## ingress

minikube addons enable ingress
minikube addons list
