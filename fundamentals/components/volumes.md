# Volumes

Volumes provide storage to containers in a Pod.

## Types

- emptyDir
- hostPath
- PersistentVolume (PV)
- PersistentVolumeClaim (PVC)

Volumes outlive container restarts but may not outlive Pods unless persistent.
