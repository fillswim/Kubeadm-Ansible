# Kubeadm-Ansible

Activate .venv 
```
source .venv/bin/activate
```
# =============== K8s1 RHEL ==============

ansible-playbook -i inventory/k8s1_rhel.yaml ping.yaml -b
ansible-playbook -i inventory/k8s1_rhel.yaml Create-LVM-Partition.yaml -b
ansible-playbook -i inventory/k8s1_rhel.yaml Install-K9s.yaml -b
ansible-playbook -i inventory/k8s1_rhel.yaml Enable-SCR.yaml -b


# ============== K8s1 Oracle =============

## Ping
ansible-playbook -i inventory/k8s1_ol.yaml Role_Ping.yaml -b

## Create Cluster 
ansible-playbook -i inventory/k8s1_ol.yaml Kubeadm_Create-Cluster.yaml -b \
ansible-playbook -i inventory/k8s1_ol.yaml Install-MetalLB.yaml -b \
ansible-playbook -i inventory/k8s1_ol.yaml Install-Helm.yaml -b \
ansible-playbook -i inventory/k8s1_ol.yaml Install-IngressController.yaml -b \
ansible-playbook -i inventory/k8s1_ol.yaml Install-K9s.yaml -b

## Reset Cluster
ansible-playbook -i inventory/k8s1_ol.yaml Kubeadm_Reset-Cluster.yaml -b \
ansible-playbook -i inventory/k8s1_ol.yaml Reboot.yaml -b

# ============== K8s1 Redos ==============

## Ping
ansible-playbook -i inventory/k8s1_redos.yaml Role_Ping.yaml -b

## Create Cluster 
ansible-playbook -i inventory/k8s1_redos.yaml Kubeadm_Create-Cluster.yaml -b \
ansible-playbook -i inventory/k8s1_redos.yaml Install-MetalLB.yaml -b \
ansible-playbook -i inventory/k8s1_redos.yaml Install-Helm.yaml -b \
ansible-playbook -i inventory/k8s1_redos.yaml Install-IngressController.yaml -b \
ansible-playbook -i inventory/k8s1_redos.yaml Install-K9s.yaml -b \
ansible-playbook -i inventory/k8s1_redos.yaml Install-Metrics-Server.yaml -b \
ansible-playbook -i inventory/k8s1_redos.yaml Install-ArgoCD.yaml -b

## Reset Cluster
ansible-playbook -i inventory/k8s1_redos.yaml Kubeadm_Reset-Cluster.yaml -b \
ansible-playbook -i inventory/k8s1_redos.yaml Reboot.yaml -b