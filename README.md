# jtprogru.memos

[![Release to Ansible Galaxy](https://github.com/jtprogru/ansible-role-memos/actions/workflows/galaxy.yml/badge.svg)](https://github.com/jtprogru/ansible-role-memos/actions/workflows/galaxy.yml)
![GitHub](https://img.shields.io/github/license/jtprogru/ansible-role-memos)
[![Ansible Role](https://img.shields.io/ansible/role/62618)](https://galaxy.ansible.com/jtprogru/memos/)
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

## Requirements

Docker with the Compose CLI plugin v2 on the target host, `community.docker` collection `>= 3.8.0` on the controller. See [`requirements.yml`](requirements.yml).

## Development

Python dependencies are managed with [uv](https://docs.astral.sh/uv/). The pinned set lives in `pyproject.toml` and `uv.lock`, the interpreter version in `.python-version`.

```bash
uv sync                 # create .venv from uv.lock
uv run ansible-lint .   # or: task anslint
task lint               # yamllint + ansible-lint
```

To bump the pinned versions run `uv lock --upgrade` (or `task lock`) and commit the updated `uv.lock`.

## Authors

- Michael Savin
  - :octocat: [@jtprogru](https://www.github.com/jtprogru)
  - :bird: [@jtprogru](https://www.twitter.com/jtprogru)
  - :moneybag: [savinmi.ru](https://savinmi.ru)

## License

See [LICENSE](LICENSE.md)
