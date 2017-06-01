Now, we let's create a [namespace](https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/) to launch applications in.

We can do this using `kubectl create` followed by `ns` for namespace, and then the name of our namespace, like so:

`
kubectl create ns policy-demo
`{{execute}}
