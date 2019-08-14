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

Flux install docs: [docs.fluxcd.io](https://docs.fluxcd.io/en/latest/tutorials/get-started-helm.html).

Install Helm Operator:

```bash
helm upgrade -i helm-operator fluxcd/helm-operator \
--namespace fluxcd \
--set createCRD=true
```

Helm Operator install docs: [docs.fluxcd.io](https://github.com/fluxcd/helm-operator/tree/master/chart/helm-operator).
