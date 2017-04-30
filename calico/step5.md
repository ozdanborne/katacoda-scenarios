The kubectl is the command line client used to communicate with the Master.

`
kubectl create -f - <<EOF
kind: Pod
apiVersion: v1
metadata:
  name: client
  namespace: policy-demo
spec:
  containers:
  - name: busybox
    image: busybox
    args:
    - sleep
    - "10000"
EOF
`{{execute}}


`
kubectl exec -n policy-demo client --
wget -T 2 -q nginx  -O -
`{{execute}}
