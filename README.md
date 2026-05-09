# Kubeadm-Ansible

Activate .venv 
```bash
source .venv/bin/activate
```

# ==============================================================================
#                                  K8s1 RHEL
# ==============================================================================
ansible-playbook -i inventory/RHEL-K8s1/k8s1-rhel.yaml ping.yaml -b

ansible-playbook -i inventory/RHEL-K8s1/k8s1-rhel.yaml Role_01-Preparation-K8s.yaml -b
ansible-playbook -i inventory/RHEL-K8s1/k8s1-rhel.yaml Create-LVM-Partition.yaml -b
ansible-playbook -i inventory/RHEL-K8s1/k8s1-rhel.yaml Install-K9s.yaml -b
ansible-playbook -i inventory/RHEL-K8s1/k8s1-rhel.yaml Enable-SCR.yaml -b
ansible-playbook -i inventory/RHEL-K8s1/k8s1-rhel.yaml Install-K9s.yaml -b
ansible-playbook -i inventory/RHEL-K8s1/k8s1-rhel.yaml Update-Calico.yaml -b
ansible-playbook -i inventory/RHEL-K8s1/k8s1-rhel.yaml Install-Helm.yaml -b
ansible-playbook -i inventory/RHEL-K8s1/k8s1-rhel.yaml Update-MetalLB.yaml -b
ansible-playbook -i inventory/RHEL-K8s1/k8s1-rhel.yaml Install-ArgoCD.yaml -b

ansible-playbook -i inventory/RHEL-K8s1/k8s1-rhel.yaml test.yaml -b > .logs/k8s1-rhel-services.log

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

ansible-playbook -i inventory/k8s1-alma.yaml Role_02-High-Availability.yaml -b

# ==============================================================================
#                              K8s2 Alma Linux 9.6
# ==============================================================================

ansible-playbook -i inventory/k8s2-alma.yaml ping.yaml -b
ansible-playbook -i inventory/k8s2-alma.yaml Kubeadm_Create-Cluster.yaml -b

ansible-playbook -i inventory/k8s2-alma.yaml Role_01-Preparation-K8s.yaml -b
ansible-playbook -i inventory/k8s2-alma.yaml Create-LVM-Partition.yaml -b

ansible-playbook -i inventory/k8s2-alma.yaml Role_06-Delete-Node.yaml -b
ansible-playbook -i inventory/k8s2-alma.yaml Kubeadm_Reset-Cluster.yaml -b
ansible-playbook -i inventory/k8s2-alma.yaml Install-Helm.yaml -b

ansible-playbook -i inventory/k8s2-alma.yaml Role_02-High-Availability.yaml -b

# ==============================================================================
#                              K8s1 Altlinux 10.4
# ==============================================================================

ansible-playbook -i inventory/k8s1-altlinux.yaml ping.yaml -b
ansible-playbook -i inventory/k8s1-altlinux.yaml Kubeadm_Create-Cluster.yaml -b

ansible-playbook -i inventory/k8s1-altlinux.yaml Role_01-Preparation-K8s.yaml -b
ansible-playbook -i inventory/k8s1-altlinux.yaml Kubeadm_Reset-Cluster.yaml -b
ansible-playbook -i inventory/k8s1-altlinux.yaml Reboot.yaml -b

# ==============================================================================
#                              Ubuntu K8s1
# ==============================================================================

ansible-playbook -i inventory/Ubuntu-K8s1/ubuntu-k8s1.yaml ping.yaml -b
<!-- ansible-playbook -i inventory/Ubuntu-K8s1/ubuntu-k8s1.yaml Kubeadm_Create-Cluster.yaml -b -->

ansible-playbook -i inventory/Ubuntu-K8s1/ubuntu-k8s1.yaml ping.yaml -b
ansible-playbook -i inventory/Ubuntu-K8s1/ubuntu-k8s1.yaml Role_01-Preparation-K8s.yaml -b

# ==============================================================================
#                                   Nexus
# ==============================================================================

ansible-playbook -i inventory/Nexus/nexus.yaml ping.yaml -b
ansible-playbook -i inventory/Nexus/nexus.yaml Install-Nexus.yaml -b

# ==============================================================================
#                           Ubuntu K8s3 (ContainerD)
# ==============================================================================

ansible-playbook -i inventory/Ubuntu-K8s3/ubuntu-k8s3.yaml ping.yaml -b
ansible-playbook -i inventory/Ubuntu-K8s3/ubuntu-k8s3.yaml Role_01-Preparation-K8s.yaml -b

# ==============================================================================
#                             Ubuntu K8s4 (CRI-O)
# ==============================================================================

ansible-playbook -i inventory/Ubuntu-K8s4/ubuntu-k8s4.yaml ping.yaml -b
ansible-playbook -i inventory/Ubuntu-K8s4/ubuntu-k8s4.yaml Role_01-Preparation-K8s.yaml -b