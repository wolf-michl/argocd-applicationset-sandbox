# argocd-applicationset-sandbox

Just a simple sandbox project to try out Argo
CD's [applicationset](https://argo-cd.readthedocs.io/en/latest/operator-manual/applicationset/) CRD and
its [generators](https://argo-cd.readthedocs.io/en/latest/operator-manual/applicationset/Generators/).

## Examples

All examples listed below can be tried by applying the corresponding applicationset CR.

```bash
kubectl apply -n argocd -f APPSET_YAML
```

CR_YAML is the path to the corresponding applicationset YAML.

### [List generator](https://argo-cd.readthedocs.io/en/latest/operator-manual/applicationset/Generators-List/) examples

#### Multiple clusters example

Our application should be deployed to multiple clusters.

```bash
kubectl apply -n argocd -f list-generated-clusters.yaml
```

#### Multiple environments example

Our application has a different state per environment, which we illustrate with multiple branches. We deploy those into
their own environment-specific namespaces.

```bash
kubectl apply -n argocd -f list-generated-environments.yaml
```

### [Cluster generator](https://argo-cd.readthedocs.io/en/latest/operator-manual/applicationset/Generators-Cluster/) example

```bash
kubectl apply -n argocd -f cluster-generated.yaml
```

### [Git generator](https://argo-cd.readthedocs.io/en/latest/operator-manual/applicationset/Generators-Git/) example

```bash
kubectl apply -n argocd -f git-generated.yaml
```

### [Matrix generator](https://argo-cd.readthedocs.io/en/latest/operator-manual/applicationset/Generators-Matrix/) example

Here we combine a git generator with a list generator.

```bash
kubectl apply -n argocd -f matrix-generated.yaml
```