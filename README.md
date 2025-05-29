# Helm charts
Charts used to deploy services to k8s.

## How use the charts
```bash
helm repo add eltio https://eltiocaballoloco.github.io/helm-charts
helm search repo eltio
helm repo update
```

## Test the output of charts
```bash
cd charts
helm template example ./main-charts -f ./main-charts/values.yaml > output.yaml
```
