The kubectl is the command line client used to communicate with the Master.

`
kubectl run --namespace=policy-demo access --rm -ti --image busybox /bin/sh
`{{execute}}

`
wget -q nginx  -O -
`{{execute}}
