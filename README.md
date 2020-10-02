# ansible-centos-server

## Purpose

The purpose of the ansible-centos-server Ansible role is to apply a basic configuration to a new CentOS server. The role is meant to be used as a base to build off of, but it can be used on its own to establish a base configuration. The role performs the following actions:

- Sets the server's hostname
- Appends a /etc/hosts entry mapping the server's IP address to the server's hostname
- Expands the root filesystem (only applies to ARM-based installations)
- Upgrades all packages
- Installs often-used packages
- Performs a server restart
