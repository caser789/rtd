namespace
==============================

## create

kubectl create  namespace my-ns


## quota

```
apiVersion: v1
kind: ResourceQuota
metadata:
  name: podquota
spec:
  hard:
    pods: "10"
```
