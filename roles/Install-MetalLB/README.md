# Install MetalLB

# K8s1-RHEL:
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Install-MetalLB.yaml -b
```

# K8s1-OL:
```bash
ansible-playbook -i inventory/k8s1_ol.yaml Install-MetalLB.yaml -b
```

# K8s1 Redos:
```bash
ansible-playbook -i inventory/k8s1_redos.yaml Install-MetalLB.yaml -b
```