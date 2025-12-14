# StatefulSets

StatefulSets are Kubernetes workload resources used to manage **stateful applications**.

Unlike Deployments, StatefulSets provide **stable network identities, persistent storage, and ordered deployment guarantees**, which are critical for databases and distributed systems.

## Key Characteristics

- Stable and unique Pod names (e.g., app-0, app-1)
- Stable network identity via Headless Services
- Persistent storage using PersistentVolumeClaims
- Ordered Pod creation, scaling, and deletion

## When to Use StatefulSets

Use StatefulSets when your application requires:

- Stable hostnames
- Persistent data tied to individual Pods
- Ordered startup and shutdown
- Leader–follower or quorum-based architectures

Examples:
- MySQL, PostgreSQL
- MongoDB
- Kafka, Zookeeper
- Elasticsearch

## StatefulSet vs Deployment

| Feature | Deployment | StatefulSet |
|-------|-----------|-------------|
| Pod Identity | Random | Stable |
| Storage | Shared / Ephemeral | Per-Pod Persistent |
| Scaling | Parallel | Ordered |
| Use Case | Stateless apps | Stateful apps |

## Architecture Components

- **StatefulSet Controller**: Manages Pod identity and lifecycle
- **Headless Service**: Provides DNS entries for each Pod
- **PVC Templates**: Automatically create PVCs per Pod

StatefulSets are commonly used in platform engineering to run core infrastructure services reliably.
