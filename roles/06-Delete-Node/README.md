# Delete Node

## K8s1-RHEL
#### Delete node Worker2
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Role_06-Delete-Node.yaml -b --extra-vars "deleted_node=k8s1-rhel-worker3.fillswim.local"
```

#### Delete node Storage 3
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Role_06-Delete-Node.yaml -b --extra-vars "deleted_node=k8s1-rhel-str-n01.fillswim.local"
```
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Role_06-Delete-Node.yaml -b --extra-vars "deleted_node=k8s1-rhel-str-n01.fillswim.local"
ansible-playbook -i inventory/k8s1_rhel.yaml Role_06-Delete-Node.yaml -b --extra-vars "deleted_node=k8s1-rhel-str-n02.fillswim.local"
ansible-playbook -i inventory/k8s1_rhel.yaml Role_06-Delete-Node.yaml -b --extra-vars "deleted_node=k8s1-rhel-str-n03.fillswim.local"
ansible-playbook -i inventory/k8s1_rhel.yaml Role_06-Delete-Node.yaml -b --extra-vars "deleted_node=k8s1-rhel-str-n04.fillswim.local"
```




## K8s2-RHEL
#### Delete node Master2
```bash
ansible-playbook -i inventory/k8s2_rhel.yaml Role_06-Delete-Node.yaml -b --extra-vars "deleted_node=k8s2-rhel-master2.fillswim.local"
```

#### Delete node Master3
```bash
ansible-playbook -i inventory/k8s2_rhel.yaml Role_06-Delete-Node.yaml -b --extra-vars "deleted_node=k8s2-rhel-master3.fillswim.local"
```

#### Delete node Worker1
```bash
ansible-playbook -i inventory/k8s2_rhel.yaml Role_06-Delete-Node.yaml -b --extra-vars "deleted_node=k8s2-rhel-worker1.fillswim.local"
```

#### Delete node Worker2
```bash
ansible-playbook -i inventory/k8s2_rhel.yaml Role_06-Delete-Node.yaml -b --extra-vars "deleted_node=k8s2-rhel-worker2.fillswim.local"
```
