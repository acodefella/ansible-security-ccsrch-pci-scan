# ccsrch-pci-scan
This Ansible project consists of a playbook, which scan servers for PCI compliance. This works only on 64-bit Linux servers.


## Prerequisites
* [Git](https://git-scm.com/) >= 2.19.1
* [Ansible](https://www.ansible.com/) >= 2.7.0
* [VirtualBox](https://www.virtualbox.org/) >= 6.0.4
* [Vagrant](https://www.vagrantup.com/) >= 2.2.4

## Usage
### Ansible
* Specify your ssh user using the `--user` flag.
* Specify your ssh target hosts using the `--inventory-file` flag.

Use Ansible to run the playbook against a target host of your choice:
```
ansible-playbook \
--user myUsername \
--ask-pass \
--ask-become-pass \
--inventory-file "<server-ip>," \
playbook.yml
```

## Development
### Vagrant
Use Vagrant to run the playbook and role and then check around:
```
vagrant up
vagrant ssh
```
