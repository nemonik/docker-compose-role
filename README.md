# Docker-compose Ansible role

![Basic role syntax check](https://github.com/nemonik/docker-compose-role/workflows/Basic%20role%20syntax%20check/badge.svg)

An Ansible role used to install docker-compose.

## Requirements

Doxckewre installed.  Consider  https://github.com/nemonik/docker-role

## Role Variables

| Variable                 | Required | Default               | Choices             | Comments                                         |
|--------------------------|----------|-----------------------|---------------------|--------------------------------------------------|
| default_retries          | yes      | 60                    | Integer value       | default number of retries                        |
| default_delay            | yes      | 60                    | Integer value       | default delay in seconds between retries         |

## Example Playbook

An example can be found used in my Hands-on DevOps course's [box/ansible/box-playbook-1.yml](https://github.com/nemonik/hands-on-DevOps/blob/master/box/ansible/box-playbook-1.yml).

```
- hosts: boxes
  connection: local
  remote_user: vagrant
  roles:
    - common
    - docker
    - docker-compose
```

The above Ansible playbook uses my

- [Common role](https://github.com/nemonik/common-role) to configure the instance past the base CentOS 7, Alpine 3.10 or Ubuntu Bionic image
- [Docker role](https://github.com/nemonik/docker-role) to install and configure Docker
- [This role](https://github.com/nemonik/docker-compose-role) to install Docker-compose

For more information and to see this role put into action checkout my [Hands-on DevOps class](https://github.com/nemonik/hands-on-DevOps) project.

## License

3-Clause BSD License

## Author Information

Michael Joseph Walsh <mjwalsh@nemonik.com>
