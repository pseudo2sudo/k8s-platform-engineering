Worker Nodes — The Data Plane
Worker nodes are machines (physical or virtual) where your applications actually run. Each worker node runs essential components to communicate with the control plane and execute workloads:

1. Pods
The smallest deployable unit in Kubernetes

One or more containers that share the same network namespace and storage

Controllers (like Deployments) create and manage Pods to achieve desired state

Containers inside Pods are managed as a single unit

2. kubelet
An agent running on each worker node

Ensures that containers described in PodSpecs are running and healthy

Reports status back to the API server

Acts as the node-level executor of workload instructions from the control plane

3. kube-proxy
Maintains networking rules on each node

Handles internal cluster networking and service-level load balancing

Routes traffic from services to the appropriate Pods

4. Container Runtime
Software that runs containers (e.g., containerd or Docker)

Responsible for pulling container images, starting containers, and managing their lifecycle

Abstracted so Kubernetes can work with multiple runtimes
