# Services

A Service provides a stable network endpoint to access Pods.

Services decouple application access from Pod lifecycle.

### Why:
- Pods are ephemeral → Services solve that
- Shows you understand **network abstraction**
## What Problems Services Solve

- Pod IPs are not stable
- Pods scale up and down
- Traffic must be load-balanced
---
## How Services Work

- Services select Pods using labels
- kube-proxy routes traffic to matching Pods
- Load balancing happens automatically

## Types of Services

- ClusterIP (default)
- NodePort
- LoadBalancer
- ExternalName
### ClusterIP (Default)
- Accessible only inside the cluster
- Used for internal communication


### NodePort
- Exposes service on each node’s IP
- Accessed via `<NodeIP>:<NodePort>`


### LoadBalancer
- Uses external cloud load balancer
- Common in managed Kubernetes


### ExternalName
- Maps Service to external DNS name


## Service vs Pod


| Feature | Pod | Service |
|------|----|---------|
| IP Stability | No | Yes |
| Load Balancing | No | Yes |
| Scaling Support | No | Yes |


Services are essential for both east–west and north–south traffic.
