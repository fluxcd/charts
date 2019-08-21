# FluxCD Helm repository

Add FluxCD repository to Helm repos:

```bash
helm repo add fluxcd https://charts.fluxcd.io
```

Install Flux:

```bash
helm upgrade -i flux fluxcd/flux \
--namespace fluxcd \
--set git.url=git@github.com:org/repo
```

For more details on installing Flux please see the [chart readme]
(https://github.com/fluxcd/flux/tree/master/chart/flux).

Install Helm Operator:

```bash
helm upgrade -i helm-operator fluxcd/helm-operator \
--namespace fluxcd \
--set createCRD=true
```

For more details on installing Flux Helm Operator please see the [chart readme]
(https://github.com/fluxcd/helm-operator/tree/master/chart/helm-operator).
