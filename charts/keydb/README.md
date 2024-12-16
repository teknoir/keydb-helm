# KeyDB Helm Chart

This chart deploys KeyDB to a Kubernetes cluster.

> The implementation of the Helm chart is right now the bare minimum to get it to work.

## Usage in Teknoir platform
Use the HelmChart to deploy the KeyDB to a Device.

```yaml
---
apiVersion: helm.cattle.io/v1
kind: HelmChart
metadata:
  name: keydb
  namespace: default
spec:
  repo: https://teknoir.github.io/keydb-helm
  chart: keydb
  targetNamespace: default
  valuesContent: |-
    # Example for minimal configuration
    
```

## Adding the repository

```bash
helm repo add teknoir-keydb https://teknoir.github.io/keydb-helm/
```

## Installing the chart

```bash
helm install keydb teknoir-keydb/keydb -f values.yaml
```