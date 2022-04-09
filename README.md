# Ansible playbooks for my homelab

## Configuring Active Directory Domain Services

Add node IP addresses in Ansible inventory `hosts` file, then run:

```bash
ansible-playbook -i hosts -e @secrets.yml.enc main.yml
```

## Secrets

Encrypt secrets file:

```bash
ansible-vault encrypt secrets.yml.enc
```

Decrypt secrets file:

```bash
ansible-vault decrypt secrets.yml.enc
```

Remove executable bit:

```bash
chmod -x secrets.yml.key
```

## WSL Troubleshooting

[Windows 10/WSL: Ansible cannot read ansible.cfg from NTFS mounts](https://github.com/ansible/ansible/issues/42388)

[warning: Insecure world writable dir /mnt/c in PATH, mode 040777](https://github.com/microsoft/WSL/issues/1426)