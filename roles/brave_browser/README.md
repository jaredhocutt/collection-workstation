Brave Browser
=============

Configures a yum repository and installs the Brave Browser.

Requirements
------------

- python >= 2.6
- python-dnf

Role Variables
--------------

| Variable        | Required | Default   | Description                                                                |
| --------------- | -------- | --------- | -------------------------------------------------------------------------- |
| `brave_channel` | &#9989;  | `release` | The channel to use. Possible options are `release`, `beta`, and `nightly`. |

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: brave_browser
      vars:
        brave_channel: release
```

License
-------

MIT

Author Information
------------------

Jared Hocutt (@jaredhocutt)
