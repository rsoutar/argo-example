# argo-example

Argo CD Example

## Install ArgoCD

```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

## Port forwarding

```
kubectl port-forward service/argocd-server -n argocd 8080:443
```

## Get Admin Password

```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```

## Argo CLI Installation

```
brew install argocd
argocd login 127.0.0.1:8080
```
