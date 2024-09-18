## Run kind
```
kind create cluster --config kind.yaml --name kind-devops-main
```

## Flannel
Flannel is deployed via a Daemonset, ensuring a flannel pod operates on each node. Leveraging local disk mounting, the initialization container copies the binary files and CNI configurations to the local disk during Pod initiation, situated respectively at /opt/cni/bin/flannel and /etc/cni/net.d/10-flannel.conflist.