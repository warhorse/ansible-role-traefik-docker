Ansible Traefik (Docker)
=========
[![CI](https://github.com/warhorse/ansible-role-traefik-docker/workflows/CI/badge.svg?event=push)](https://github.com/warhorse/ansible-role-traefik-docker/actions?query=workflow%3ACI)
[![warhorse.traefik_docker](https://img.shields.io/ansible/role/57521)](https://galaxy.ansible.com/warhorse/traefik_docker)
[![warhorse.traefik_docker](https://img.shields.io/ansible/quality/57521)](https://galaxy.ansible.com/warhorse/traefik_docker)
[![warhorse.traefik_docker](https://img.shields.io/ansible/role/d/57521)](https://galaxy.ansible.com/warhorse/traefik_docker)
![License](https://img.shields.io/github/license/warhorse/ansible-role-traefik-docker)
![Commit](https://img.shields.io/github/last-commit/warhorse/ansible-role-traefik-docker)

![Traefik Logo](./images/traefik_logo.png "Traefik Logo")

Install Traefik (Docker)

This role is part of the Warhorse Automation Framework. This role can be used with Warhorse or as a standalone role.

Docker Image
-------------

[traefik](https://github.com/traefik/traefik)

Role Variables
--------------

A list of all the variables can be found in ./defaults/main.yml.

`traefik_dir` - Traefik container directory 

`traefik_docker_version` - Docker image version

`traefik_ports` - Traefik container ports

`traefik_hostname` - Traefik container hostname

`traefik_container_name` - Traefik container name 

`traefik_docker_network` - Traefik container docker network


Dependencies
------------

```shell
ansible-galaxy install geerlingguy.docker geerlingguy.pip
```

Install
------------

```shell
ansible-galaxy install warhorse.traefik_docker
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
      - { role: warhorse.traefik_docker }
```

Example Vars
----------------

```yaml
traefik_hostname: "traefik"
traefik_container_name: "traefik"
traefik_docker_version: "latest"
traefik_docker_labels: {}
traefik_docker_network: "traefik"
traefik_dir: '/opt/docker/traefik'
traefik_ports:
  - '80:80'
  - '443:443'
```

License
-------

MIT/BSD

Author Information
------------------

Ralph May
