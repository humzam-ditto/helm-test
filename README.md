# helm-test

Sample Helm chart for Harness deploy testing.

## Chart: `sample-app`

Deploys an nginx-based app with a Deployment and Service. Ingress and HPA are opt-in via `values.yaml`.

## Usage

```bash
helm install my-release ./
```

## Key values

| Key | Default | Description |
|-----|---------|-------------|
| `image.repository` | `nginx` | Container image |
| `image.tag` | `stable` | Image tag |
| `replicaCount` | `1` | Number of replicas |
| `service.type` | `ClusterIP` | Kubernetes service type |
| `ingress.enabled` | `false` | Enable ingress |
| `autoscaling.enabled` | `false` | Enable HPA |
