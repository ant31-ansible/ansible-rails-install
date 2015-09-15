Rails-install
==========

Install a rails/ruby application.

Requirements
------------

 - ruby


Role Variables
---------------

```yaml
---
git_repo: "configure_your_git_repo"
git_tag: master
insall_dir: /opt/rails-app
deploy_key: "your private deploy string"
deploy_key_dir: "/tmp"

system_envs:
  RAILS_ENV: production
```

Dependencies
------------

- none

Example Playbook
----------------

```yaml
---
- hosts: rails-host
  roles:
  - role: rails-install
    ruby_version: rbx-2.1.0
    git_repo: git@mygit/app
    git_tag: stable/2.3
    deploy_key: "{{ lookup('file', 'private_key'}}"

```

License
-------

MIT
