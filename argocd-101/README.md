# ArgoCD

## Instalação

- Instalando o ArgoCD
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

- Criando um Ingress Resource

> Considerando que você já tem o ingress funcionando no seu cluster

```
kubectl apply -n argocd -f ingress.yaml
```

- Recuperando a senha inicial

```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```

- Acesse via browser

https://seuhost

> Usuário padrão é `admin`



