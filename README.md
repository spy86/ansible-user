Role Name
=========

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

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
