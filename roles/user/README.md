# User

# Install passlib
```bash
pip install passlib
```

# Зашифровать переменную, скопировать в vars/main.yaml
```bash
ansible-vault encrypt_string '123456' --name 'upassword'
```

## Запуск:
```bash
ansible-playbook -i inventory/k8s1_rhel.yaml user.yaml --ask-vault-pass -b
```