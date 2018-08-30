deployment
==============================

## create

* the generator way

```
kubectl run ghost --image=ghost:0.9
kubectl run nginx --image=nginx
kubectl run mysql --image=mysql:5.5 --env=MYSQL_ROOT_PASSWORD=root
kubectl run myshell --image=busybox --command -- sh -c "sleep 3600"
```

## update

```
kubectl edit deploy/nginx
kubectl set image
```

## rollout

kubectl rollout undo deployment sise --to-revision=2
