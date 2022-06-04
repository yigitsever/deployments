# Deployments

First, check if you have `kubectl` access;

```bash
kubectl get nodes
```

Check whether the deployment does already exist;

```bash
kubectl get deployments
```

If not, apply

```bash
kubectl apply -f <cve>-deployment.yaml
kubectl apply -f <cve>-service.yaml
```

## Creating a New Deployment and Service

Ports `30000` through `30050` are exposed on k3s.

Pick an unused (lowest) port;

```bash
kubectl get services
```

Create `<cve>-deployment.yaml` and `<cve>-service.yaml` accordingly.

## References
- https://k3d.io/v5.1.0/usage/exposing_services/
