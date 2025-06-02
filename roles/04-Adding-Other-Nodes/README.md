# Adding Other Nodes

## K8s1-RHEL (add all nodes of inventory)
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Role_04-Adding-Other-Nodes.yaml -b
```

#### Добавление одной Str1 ноды
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Role_04-Adding-Other-Nodes.yaml -b --extra-vars "added_node=k8s1-rhel-str-n01.fillswim.local"
```
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Role_04-Adding-Other-Nodes.yaml -b --extra-vars "added_node=k8s1-rhel-str-n02.fillswim.local"
```
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Role_04-Adding-Other-Nodes.yaml -b --extra-vars "added_node=k8s1-rhel-str-n03.fillswim.local"
```
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Role_04-Adding-Other-Nodes.yaml -b --extra-vars "added_node=k8s1-rhel-str-n04.fillswim.local"
```
Worker 3
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Role_04-Adding-Other-Nodes.yaml -b --extra-vars "added_node=k8s1-rhel-worker3.fillswim.local"
```
Worker 4
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Role_04-Adding-Other-Nodes.yaml -b --extra-vars "added_node=k8s1-rhel-worker4.fillswim.local"
```


## K8s2-RHEL (add all nodes of inventory)
```bash
ansible-playbook -i inventory/k8s2_rhel.yaml Role_04-Adding-Other-Nodes.yaml -b
```



## K8s2-RHEL
#### Добавление одной Master2 ноды
```bash
ansible-playbook -i inventory/k8s2_rhel.yaml Role_04-Adding-Other-Nodes.yaml -b --extra-vars "added_node=k8s2-rhel-master2.fillswim.local"
```

#### Добавление одной Master3 ноды
```bash
ansible-playbook -i inventory/k8s2_rhel.yaml Role_04-Adding-Other-Nodes.yaml -b --extra-vars "added_node=k8s2-rhel-master3.fillswim.local"
```

#### Add only one Worker1 node
```bash
ansible-playbook -i inventory/k8s2_rhel.yaml Role_04-Adding-Other-Nodes.yaml -b --extra-vars "added_node=k8s2-rhel-worker1.fillswim.local"
```

#### Add only one Worker2 node
```bash
ansible-playbook -i inventory/k8s2_rhel.yaml Role_04-Adding-Other-Nodes.yaml -b --extra-vars "added_node=k8s2-rhel-worker2.fillswim.local"
```



## K8s1 Redos (add all nodes of inventory)
```bash
ansible-playbook -i inventory/k8s1_redos.yaml Role_04-Adding-Other-Nodes.yaml -b
```