Ansible Role: Visual Studio Code Extensions
===========================================
Like [gantsign.visual-studio-code-extensions](https://galaxy.ansible.com/gantsign/visual-studio-code-extensions/) but for OS X.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/donaldaverill/ansible-role-visual-studio-code-extensions/master/LICENSE)

Role to install extensions for the
[Visual Studio Code](https://code.visualstudio.com) IDE / text editor.

Requirements
------------

* Ansible >= 2.0

* OS X

Role Variables
--------------

The following variables will change the behavior of this role (default values
are shown below):

```yaml
# Users to install extensions for
users: []
```

Users are configured as follows:

```yaml
users:
  - username: # Unix user name
    visual_studio_code_extensions:
      - # extension 1
      - # extension 2
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: gantsign.visual-studio-code-extensions
      users:
        - username: vagrant
          visual_studio_code_extensions:
            - streetsidesoftware.code-spell-checker
            - wholroyd.jinja
            - donjayamanne.python
```

License
-------

MIT

Author Information
------------------

John Freeman

GantSign Ltd.
Company No. 06109112 (registered in England)
