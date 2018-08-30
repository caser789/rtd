NodePort vs LoadBalancer vs Ingress
========================================

## Common

* get external traffic into cluster


## ClusterIP

* internal access
* default service
* kubectl proxy --port=8080 (enable external access)
* `http://localhost:8080/api/v1/proxy/namespaces/<NAMESPACE>/services/<SERVICE-NAME>:<PORT-NAME>/`
* `http://localhost:8080/api/v1/proxy/namespaces/default/services/my-internal-service:http/`

![ClusterIP](nodeport_loadbalancer_ingress/ClusterIP.png)

## NodePort

* open a port (30000–32767) in every node
* only one service per port
* If your Node/VM IP address change, you need to deal with that

![NodePort](nodeport_loadbalancer_ingress/NodePort.png)

## LoadBalancer

* standard way
* send any kind of traffic to it, like HTTP, TCP, UDP, Websockets, gRPC, or whatever.
* expensive

![LoadBalancer](nodeport_loadbalancer_ingress/LoadBalancer.png)

## Ingress

* not a service

![Ingress](nodeport_loadbalancer_ingress/Ingress.png)

refs

* [blog](https://medium.com/google-cloud/kubernetes-nodeport-vs-loadbalancer-vs-ingress-when-should-i-use-what-922f010849e0)
