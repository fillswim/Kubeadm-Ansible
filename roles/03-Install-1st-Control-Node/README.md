# Install 1st Control Node

## K8s1-RHEL:
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Role_03-Install-1st-Control-Node.yaml -b
```

## K8s2-RHEL:
```bash
ansible-playbook -i inventory/k8s2_rhel.yaml Role_03-Install-1st-Control-Node.yaml -b
```