# Ansible Role - Docker

Ansible role to install docker-ce (with apt) and docker-compose (with pip)

## Configure Versions

Use the following variables to customise the versions installed:

```
docker_version: 17.06.2~ce-0~ubuntu 
docker_compose_version: 1.15.0
```

## Insecure Registries

To include insecure registries in the `/etc/docker/daemon.json` file list them under the `docker_insecure_registries` variable:

```
docker_insecure_registries:
  - myregistry:5000
  - myotherregistry:5002
```

This role will append the listed registries, meaning any existing insecure registries (or any other settings) in your `daemon.json` will remain
