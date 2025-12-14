# Ingress

Ingress is a Kubernetes API object that manages **external HTTP and HTTPS access** to services inside a cluster.

It provides **Layer 7 (application-level) routing** based on hostnames and paths, acting as the entry point for user traffic.

## Why Ingress Is Needed

Without Ingress:
- Each service requires a NodePort or LoadBalancer
- External exposure becomes expensive and hard to manage

Ingress solves this by:
- Centralizing routing rules
- Reducing the number of external load balancers
- Enabling TLS termination

## Ingress Components

### Ingress Resource

- Defines routing rules (host/path → service)
- Stored as YAML in the cluster
- Does not handle traffic by itself

### Ingress Controller

- Actual implementation that processes traffic
- Watches Ingress resources via the API server
- Examples:
  - NGINX Ingress Controller
  - Traefik
  - HAProxy
  - AWS ALB Ingress Controller

Without an Ingress Controller, Ingress resources do nothing.

## Basic Ingress Workflow

1. User sends request to external IP / DNS
2. Traffic reaches Ingress Controller
3. Controller evaluates Ingress rules
4. Request is routed to the correct Service
5. Service forwards traffic to Pods

## Ingress vs Service

| Feature | Service | Ingress |
|------|--------|---------|
| OSI Layer | L4 | L7 |
| Routing | IP/Port based | Host/Path based |
| TLS Termination | No | Yes |
| External Access | Limited | Advanced |

## Common Use Cases

- Exposing web applications
- Path-based routing (/api, /app)
- Hosting multiple domains on one cluster
- TLS termination and HTTPS enforcement

## Platform Engineering Perspective

Ingress is critical for:
- Multi-tenant clusters
- Secure north–south traffic control
- Centralized certificate management
- Integration with DNS and external load balancers

Ingress is often paired with cert-manager for automated TLS.
