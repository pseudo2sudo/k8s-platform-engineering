Control Plane — The Brain of Kubernetes

The Control Plane makes the global decisions about the cluster (e.g., scheduling pods, scaling applications) and tracks the cluster state. It includes these core components:

1. API Server (kube-apiserver)

Central access point for all REST API calls made to the cluster

Validates, authorizes, and processes requests from users or other components

All internal communication inside Kubernetes flows through this API server

It updates the persistent store (etcd) with cluster state changes

It is the core interface used by tools like kubectl 

2. Scheduler (kube-scheduler)

Watches for newly created Pods that have no assigned node

Decides where (which node) a Pod should run based on resource requirements, constraints, and policies

Ensures efficient utilization of nodes 

3. Controller Manager (kube-controller-manager)

Runs controller processes that regulate the cluster state

Examples of controllers:

NodeController — manages node status

ReplicaSetController — ensures desired replica counts

DeploymentController — updates Pods or rollbacks

Responsible for continuous reconciliation of actual vs desired state 

4. etcd

A distributed key-value store

Stores all cluster configuration and state data

Acts as the single source of truth for the entire cluster

Highly available clusters usually run multiple replicas of etcd

If etcd fails, the control plane can’t determine desired state
