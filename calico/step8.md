With these steps completed the cluster is now running along with DNS and a UI. You can check the health running the following commands.

`
kubectl run --namespace=policy-demo access --rm -ti --image busybox /bin/sh
`{{execute}}
