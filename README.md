Kubernetes Redis Cluster
========================

#### Usage:

`kubectl create -f redis.yaml`

`kubectl create -f redis-trib.yaml`

Check everything is up:

`kubectl get pods`

Should display something like this after a few minutes:

```
NAME                          READY     STATUS      RESTARTS   AGE
redis-node-7b994b89bc-5djbr   1/1       Running     0          4m
redis-node-7b994b89bc-b8fp5   1/1       Running     0          4m
redis-node-7b994b89bc-lfnt9   1/1       Running     0          4m
redis-node-7b994b89bc-p8lkb   1/1       Running     0          4m
redis-node-7b994b89bc-s272j   1/1       Running     0          4m
redis-node-7b994b89bc-xbx5b   1/1       Running     0          4m
redis-trib-96x4j              0/1       Completed   0          48s
```

Afterwards you can safely do a `kubectl delete -f redis-trib.yaml` to get rid of the leftover pod from the job.

#### Todo's:

* Add persistent storage
* Cleanup the entrypoint stuff