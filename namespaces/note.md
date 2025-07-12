# Namespace command

Default namespace

```bash
kubectl config set-context --current --namespace=<name>
```

Get config view

```bash
kubectl config view
```

Get all namespace (use namespace or ns)

```bash
kubectl get namespace --all-namespace
```

Get resource all namespace

```bash
kubectl get <resource> --all-namespace
```

Get multiple resource

```bash
kubectl get pod,svc,ns
```
