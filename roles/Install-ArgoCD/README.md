# Install Argo CD

Логин:
```bash
admin
```
Пароль:
```bash
kubectl -n argo-cd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```

## K8s1-Redos:
```bash
ansible-playbook -i inventory/k8s1_redos.yaml Install-ArgoCD.yaml -b
```