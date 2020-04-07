# ansible-monitorix

Basic Ansible Playbook to install and configure Monitorix on CentOS systems. 

By default this playbook will install the EPEL Repo, as well as configure firewalld. If you would like to change this, please modify the variables in main.yaml

- firewalld
- epel

Simple way to run against your hosts file as root with SSH password...
```
ansible-playbook -i ../hosts main.yml -k
```

Example hosts file disabling Key Checking...
```
192.168.0.2[0:5]

[all:vars]
ansible_ssh_extra_args='-o StrictHostKeyChecking=no'
```
