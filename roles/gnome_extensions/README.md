Gnome Extensions
================

Installs the specified Gnome Shell extensions.

Requirements
------------

None

Role Variables
--------------



Dependencies
------------

| Variable        | Required | Default   | Description                                                                |
| --------------- | -------- | --------- | -------------------------------------------------------------------------- |
| `gnome_extension_ids` | &#9989;  | `[]]` | A list of Gnome Shell extension IDs to install.<br><br>The extension ID can be found in the URL on https://extensions.gnome.org/. For example, the TopIcons Plus URL is https://extensions.gnome.org/extension/1031/topicons/ and the extension ID is `1031`. |

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: gnome_extensions
      vars:
        gnome_extension_ids:
          - 964
          - 770
```

License
-------

MIT

Author Information
------------------

Jared Hocutt (@jaredhocutt)
