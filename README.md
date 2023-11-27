# Helm Chart Repository

This repository hosts the Helm charts of the organisation

## Adding the Helm Repository
	
```helm repo add org-charts https://yorgosbas.github.io/helm-charts/```
	
## Usage
Any modifications made in this repository are automatically synchronized with Argo CD, ensuring seamless and immediate deployment updates for applications within our Kubernetes clusters

## Helm Index
https://yorgosbas.github.io/helm-charts/index.yaml

## Requirements
[Docker:latest](https://docs.docker.com/engine/install/)
[Kind:latest](https://kind.sigs.k8s.io/docs/user/quick-start/#installation)
[Helm v3](https://helm.sh/docs/intro/install/#through-package-managers)
[Argo:latest](https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd)
