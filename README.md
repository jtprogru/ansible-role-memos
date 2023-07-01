# jtprogru.memos

[![Ansible Molecule](https://github.com/jtprogru/ansible-role-memos/actions/workflows/molecule.yml/badge.svg)](https://github.com/jtprogru/ansible-role-memos/actions/workflows/molecule.yml)
[![Release to Ansible Galaxy](https://github.com/jtprogru/ansible-role-memos/actions/workflows/galaxy.yml/badge.svg)](https://github.com/jtprogru/ansible-role-memos/actions/workflows/galaxy.yml)
[![TODO 2 Issue](https://github.com/jtprogru/ansible-role-memos/actions/workflows/todo.yml/badge.svg)](https://github.com/jtprogru/ansible-role-memos/actions/workflows/todo.yml)
![GitHub](https://img.shields.io/github/license/jtprogru/ansible-role-memos)
[![Ansible Role](https://img.shields.io/ansible/role/54362)](https://galaxy.ansible.com/jtprogru/ansible-role-memos/)
[![GitHub tag](https://img.shields.io/github/tag/jtprogru/ansible-role-memos.svg)](https://github.com/jtprogru/ansible-role-memos/tags)

Simple ansible role for running dockerized [memos](https://usememos.com)

## Role Variables

See [`defaults/main.yml`](defaults/main.yml).

## Example Playbook

Example playbook:

```yaml
---
- name: Deploy memos
  hosts: memos.example.com
  become: true

  vars:
    memos_version: latest
    memos_volume_path: /opt/memos

  roles:
    - jtprogru.memos
```

## Authors

- Michael Savin
  - :octocat: [@jtprogru](https://www.github.com/jtprogru)
  - :bird: [@jtprogru](https://www.twitter.com/jtprogru)
  - :moneybag: [savinmi.ru](https://savinmi.ru)

## License

See [LICENSE](LICENSE.md)
