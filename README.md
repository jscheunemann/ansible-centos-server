# ansible-centos-server

## Purpose

The purpose of the ansible-centos-server Ansible role is to apply a basic configuration to a new CentOS server. The role is meant to be used as a base to build off of, but it can be used on its own to establish a base configuration. The role performs the following actions:

- Sets the server's hostname
- Appends an /etc/hosts entry, mapping the server's IP address to the server's hostname
- Expands the root filesystem (only applies to ARM-based installations)
- Upgrades all packages
- Installs often-used packages
- Performs a server restart

## Variables

The following is a list of variables that are configured in ansible-centos-server/vars/main.yml. These variables can be changed in main.yml or overridden using the ansible-playbook command.

```
server_name: "centos-server.home"
```

## Example Playbook

The following is an example Ansible playbook for running the ansible-centos-server role.
```
---
- name: apply
  hosts: all
  gather_facts: yes
  become: yes
  roles:
    - ansible-centos-server

```

## ansible-playbook example

To run the example playbook execute the following command. This assumes you saved the playbook as ansible-centos-server.yml inside of the ansible folder in the root of your user directory.

```
ansible-playbook -i "192.168.1.100," ~/ansible/ansible-centos-server.yml --ask-pass --user root
```
