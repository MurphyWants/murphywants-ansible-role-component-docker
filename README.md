# murphywants-ansible-role-component-docker

## Purpose
The purpose of this role is to create an easily re-usable ansible role to install docker and configure. Currently it is barebones, this project will grow as my homelab requirements grow.

## Changes
This ansible role currently:
- Installs docker, docker compose and dependncies 
- Configures the default bridge IP, configurable with the variable COMPONENT_DOCKER_BRIDGE_IP
  - Docker will auto create interfaces with subnets that "are not being used" on the host. However, due to my network setup the default bridge network was assigning itself to a subnet I use elsewhere.
  - https://support.hyperglance.com/knowledge/changing-the-default-docker-subnet


## Variables

Variable | Default Value | Description 
---|---|---
COMPONENT_DOCKER_BRIDGE_IP | "10.255.0.1/24" | Assigns the bridge subnet using CIDR notation

## Requirements:
This project should work with the builtin ansible roles.

## TODO
- Configure logging