# Kubeadm-Ansible

Activate .venv 
```bash
source .venv/bin/activate
```

# ==============================================================================
#                                  K8s1 RHEL
# ==============================================================================
ansible-playbook -i inventory/k8s1_rhel.yaml ping.yaml -b

ansible-playbook -i inventory/k8s1_rhel.yaml Role_01-Preparation-K8s.yaml -b
ansible-playbook -i inventory/k8s1_rhel.yaml Create-LVM-Partition.yaml -b
ansible-playbook -i inventory/k8s1_rhel.yaml Install-K9s.yaml -b
ansible-playbook -i inventory/k8s1_rhel.yaml Enable-SCR.yaml -b
ansible-playbook -i inventory/k8s1_rhel.yaml Install-K9s.yaml -b
ansible-playbook -i inventory/k8s1_rhel.yaml Update-Calico.yaml -b
ansible-playbook -i inventory/k8s1_rhel.yaml Install-Helm.yaml -b
ansible-playbook -i inventory/k8s1_rhel.yaml Update-MetalLB.yaml -b
ansible-playbook -i inventory/k8s1_rhel.yaml Install-ArgoCD.yaml -b

# ==============================================================================
#                                  K8s1 Alma VM
# ==============================================================================

ansible-playbook -i inventory/k8s1-alma-vm.yaml ping.yaml -b

# ==============================================================================
#                                  K8s1 Alma LXC
# ==============================================================================

ansible-playbook -i inventory/k8s1-alma-lxc.yaml ping.yaml -b

# ==============================================================================