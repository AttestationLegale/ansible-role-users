# Ansible Role: Users

[![Build Status](https://travis-ci.org/AttestationLegale/ansible-role-users.svg?branch=master)](https://travis-ci.org/AttestationLegale/ansible-role-users) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-users-blue.svg)](https://galaxy.ansible.com/AttestationLegale/users/)

Manage unix `users and groups`.

## Requirements

None

## Role Variables

For a complete list of variables, see `default/main.yml`.

    users
    groups
    users_deleted

## Dependencies

None

## Example Playbook

```yaml
---
  - hosts: all
    roles:
      - users
    vars:
      users:
        - username: foo
          name: Foo Barrington
          groups: ['wheel','systemd-journal']
          uid: 1001
          ssh_key: "ssh-rsa AAAAB.... foo2@machine"
    users_deleted:
      - username: bar
```

## License

MIT / BSD

## Author Information

This role was created in 2016 by [ALG](https://www.attestationlegale.fr), based on a fork of [ansible-users](https://github.com/mivok/ansible-users)
