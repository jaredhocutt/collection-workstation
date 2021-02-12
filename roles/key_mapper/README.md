Key Mapper
==========

Installs Key Mapper from https://github.com/sezanzeb/key-mapper.

Requirements
------------

- python >= 2.6
- python-dnf

Role Variables
--------------

| Variable             | Required | Default | Description                                                                                                                                                                             |
| -------------------- | -------- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `key_mapper_version` | &#9989;  | `main`  | The version of Key Mapper to install.<br><br>Using `latest` will always download the latest version of Ferdi. You can select a specific version from the Key Mapper [releases page][1]. |

[1]: https://github.com/sezanzeb/key-mapper/releases

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: key_mapper
      vars:
        key_mapper_version: 0.6.1
```

License
-------

MIT

Author Information
------------------

Jared Hocutt (@jaredhocutt)
