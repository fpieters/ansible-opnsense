# ansible-opnsense
Ansible playbooks to automate OPNSense installs

# Prepare FreeBSD for Ansible:

```
echo 'sshd_enable="YES"' >> /etc/rc.conf
service sshd start
pkg install sudo
echo '%wheel ALL=(ALL) ALL' >/usr/local/etc/sudoers.d/allow-wheel-user-login
pkg install python27
```

# Ansible:
- Clone this repo and run the playbook(s):
```
ansible-playbook api.yml -i hosts --ask-vault-pass
ansible-playbook config.yml -i hosts
ansible-playbook template.yml -i hosts
```
