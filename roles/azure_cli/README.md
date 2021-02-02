Azure CLI
=========

Configures the Azure CLI repository and installs Azure CLI.

Requirements
------------

- python >= 2.6
- python-dnf

Role Variables
--------------

None

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: azure_cli
```

License
-------

MIT

Author Information
------------------

Jared Hocutt (@jaredhocutt)
