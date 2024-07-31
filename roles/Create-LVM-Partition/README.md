# Create LVM Partition

! Поменять в файле "Create-LVM-Partition.yaml" группу
```bash
- name: Create LVM Partition
  # hosts: k8s_workers
  hosts: nexus

  roles:
    - role: Create-LVM-Partition
```

## K8s1-RHEL:
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml Create-LVM-Partition.yaml -b
```

## Nexus:
```bash
ansible-playbook -i inventory/nexus_servers.yaml Create-LVM-Partition.yaml -b
```

## Repository Ubuntu:
```bash
ansible-playbook -i inventory/repository-ubuntu.ini Create-LVM-Partition.yaml -b
```

## Repository Oracle Linux:
```bash
ansible-playbook -i inventory/repository-ol.ini Create-LVM-Partition.yaml -b
```