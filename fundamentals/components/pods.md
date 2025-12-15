## Purpose
Explain what a Pod is and why Kubernetes schedules Pods instead of containers.

Pods are ephemeral by nature and are usually managed by higher-level controllers like Deployments or StatefulSets.

# Pods

A Pod is the smallest deployable unit in Kubernetes.

## Characteristics

- One or more containers
- Shared network namespace
- Shared storage volumes
- Scheduled on a single node

## Pod Networking
- One IP address per Pod
- Containers communicate via `localhost`
- Pod-to-Pod communication is flat (no NAT)

## Pod Lifecycle
- Pending
- Running
- Succeeded
- Failed
- Unknown

## Restart Policy
- Always
- OnFailure
- Never

## Common Failure Scenarios
- ImagePullBackOff
- CrashLoopBackOff
- OOMKilled

## Basic Commands
```bash
kubectl get pods
kubectl describe pod <pod-name>
kubectl logs <pod-name>
