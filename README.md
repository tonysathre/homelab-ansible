# homelab-ansible
Ansible playbooks for my homelab

## Configuring Active Directory Domain Services

Add node IP addresses in Ansible inventory `hosts` file, then run:

```bash
ansible-playbook -i hosts main.yml
```