service
==============================

## create

### the generator way

```
kubectl expose deployments ghost --port=2368 --type=NodePort
kubectl expose deploy/nginx --port 80
```

## proxy

kubectl proxy
open http://localhost:8001/api/v1/proxy/namespaces/default/services/nginx/

## dns

$service_name.$namespace.svc.cluster.local

kubectl run busybox --image busybox -it -- /bin/sh

nslookup nginx
