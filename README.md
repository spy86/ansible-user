Role Name
=========

![ansible-user](https://img.shields.io/github/issues/spy86/ansible-user.svg) ![ansible-user](https://img.shields.io/github/forks/spy86/ansible-user.svg) ![ansible-user](https://img.shields.io/github/stars/spy86/ansible-user.svg) ![ansible-user](https://img.shields.io/github/license/spy86/ansible-user.svg) ![ansible-user](https://img.shields.io/twitter/url/https/github.com/spy86/ansible-user.svg?style=social)

Ansible role to set up users and groups.

Requirements
------------

None

Role Variables
--------------

## 'users_group'

- list of groups that will be created

## 'users'


**Required**

- `password` 

**Optional**

- `group`
- `groups`
- `ssh_keys` 
- `ssh_keys_url`
- `generate_ssh_key`
- `ssh_key_public`
- `ssh_key_private`
- `ps1`

Dependencies
------------

None

Example Playbook
----------------

```yaml
---
users_groups:
  - superadmins
  - secondgroup
users:
  smeuser:
    password: Itt1k|*Jmdi$15m3HnyRo!fZG*Fm&xtE-YS"Ub?sHSVp"W?SICle^?6D@.PKQ:LX,,L,~PgbPT"r&#j1mrP&W!x\!WZSgOUo7h?k!0EPLEKsBzdz_+\H/,JFur/HV@10
    ssh_keys_url: https://some-url.com/ssh-keys
    generate_ssh_key: yes
    group: superadmins
    groups:
      - secondgroup
      - sudo
```
