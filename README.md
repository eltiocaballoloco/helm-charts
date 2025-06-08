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
helm template \
  --release-name hello-world-1 \
  ./main-charts \
  --namespace hello-app \
  -f ./main-charts/values.yaml > output.yaml
```

## Using charts locally
To use the charts locally it is possible execute the following command
```bash
helm template --debug --dry-run \
--set debug=true \
--release-name your-app-name \
--namespace your-namespace \
--repo https://eltiocaballoloco.github.io/helm-charts \
-f values.yaml \
-f local-secret.yaml \
main-charts > output.yaml
```