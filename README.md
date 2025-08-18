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
#                              K8s1 Alma Linux 9.6
# ==============================================================================

ansible-playbook -i inventory/k8s1-alma.yaml ping.yaml -b
ansible-playbook -i inventory/k8s1-alma.yaml Kubeadm_Create-Cluster.yaml -b

ansible-playbook -i inventory/k8s1-alma.yaml ssh-key-hosts.yaml -b
ansible-playbook -i inventory/k8s1-alma.yaml Install-Helm.yaml -b
ansible-playbook -i inventory/k8s1-alma.yaml Install-K9s.yaml -b

ansible-playbook -i inventory/k8s1-alma.yaml Role_06-Delete-Node.yaml -b
ansible-playbook -i inventory/k8s1-alma.yaml Kubeadm_Reset-Cluster.yaml -b

# ==============================================================================
#                              K8s1 Alma Linux 9.6
# ==============================================================================

ansible-playbook -i inventory/k8s1-altlinux.yaml ping.yaml -b
ansible-playbook -i inventory/k8s1-altlinux.yaml Kubeadm_Create-Cluster.yaml -b

# ==============================================================================
