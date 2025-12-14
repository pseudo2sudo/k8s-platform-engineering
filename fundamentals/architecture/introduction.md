What is Kubernetes?

Kubernetes (often abbreviated K8s) is an open-source container orchestration platform originally developed by Google and now maintained by the Cloud Native Computing Foundation. It automates deployment, scaling, and management of containerized applications across clusters of machines. 

At its core, Kubernetes enables you to define a desired state for your application (for example, number of replicas, resource limits, etc.) and ensures the actual state matches that desired state through reconciliation.

Why Kubernetes? (What Problems It Solves)

Kubernetes addresses key operational challenges when running containerized applications in production:

Automated deployment and rollback

Scaling applications up or down

Load balancing of traffic to containers

Self-healing (restarting failed containers, rescheduling)

Service discovery and networking inside clusters

Resource optimization across machines

This automation reduces manual toil and improves reliability and uptime

Kubernetes Architecture Overview

A Kubernetes system (a cluster) consists of two main logical parts:

A. Control Plane (Master)
B. Worker Nodes (Data Plane)

Together, they manage and run containerized workloads
