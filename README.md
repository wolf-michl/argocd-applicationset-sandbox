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

### [List generator example](https://argo-cd.readthedocs.io/en/latest/operator-manual/applicationset/Generators-List/)

```bash
kubectl apply -n argocd -f list-generated.yaml
```

### [Cluster generator example](https://argo-cd.readthedocs.io/en/latest/operator-manual/applicationset/Generators-Cluster/)

```bash
kubectl apply -n argocd -f cluster-generated.yaml
```

### [Git generator example](https://argo-cd.readthedocs.io/en/latest/operator-manual/applicationset/Generators-Git/)

```bash
kubectl apply -n argocd -f git-generated.yaml
```

### [Matrix generator example](https://argo-cd.readthedocs.io/en/latest/operator-manual/applicationset/Generators-Matrix/)

Here we combine a git generator with a list generator.

```bash
kubectl apply -n argocd -f matrix-generated.yaml
```