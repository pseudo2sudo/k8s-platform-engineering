# Deployments

Deployments manage stateless applications in Kubernetes.
A **Deployment** is a higher-level Kubernetes controller used to manage **stateless applications**.
It ensures the desired number of Pods are running and handles updates automatically.

## Responsibilities

- Create and manage ReplicaSets
- Ensure desired number of Pods
- Enable rolling updates and rollbacks

Deployments provide declarative updates for Pods and ReplicaSets.

## Deployment Workflow

1. User applies Deployment manifest
2. Deployment creates a ReplicaSet
3. ReplicaSet creates Pods
4. Controller monitors health

## Key Features

- Declarative updates
- Zero-downtime rolling updates
- Easy scaling
- Rollback to previous versions

## Deployment vs Pod

| Feature | Pod | Deployment |
|------|----|-----------|
| Self-healing | No | Yes |
| Scaling | Manual | Automatic |
| Updates | Recreate | Rolling |


Deployments are the **default choice** for running web apps and APIs in Kubernetes.
