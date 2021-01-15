Ferdi
=====

Installs Ferdi.

Requirements
------------

- python >= 2.6
- python-dnf

Role Variables
--------------

| Variable        | Required | Default  | Description                                                                                                                                                                                                                               |
| --------------- | -------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ferdi_version` | &#9989;  | `latest` | The version of Ferdi to install.<br><br>Using `latest` will always download the latest version of Ferdi. You can select a specific version from the Ferdi [releases page][1] (e.g. to install Ferdi 5.5.0, set this variable to `v5.5.0`) |

[1]: https://github.com/getferdi/ferdi/releases

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: ferdi
      vars:
        ferdi_version: v5.5.0
```

License
-------

MIT

Author Information
------------------

Jared Hocutt (@jaredhocutt)
