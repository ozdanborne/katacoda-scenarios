Allow Access using a Network Policy.

`
kubectl create -f - <<EOF
kind: NetworkPolicy
apiVersion: extensions/v1beta1
metadata:
  name: access-nginx
  namespace: policy-demo
spec:
  podSelector:
    matchLabels:
      run: nginx
  ingress:
    - from:
      - podSelector:
          matchLabels:
            run: client
EOF
`{{execute}}

`
kubectl exec -n policy-demo client -- wget -q nginx  -T 2 -O -
`{{execute}}
