Common
======

Applies the common configurations that I use for my workstations.

Requirements
------------

- python >= 2.6
- python-dnf

Role Variables
--------------

| Variable               | Required | Default | Description                                                                                                   |
| ---------------------- | -------- | ------- | ------------------------------------------------------------------------------------------------------------- |
| `packages`             | &#9989;  | `[]`    | The list of packages to install.                                                                              |
| `flatpaks`             | &#9989;  | `[]`    | The list of flatpaks to install from Flathub.                                                                 |
| `services`             | &#9989;  | `[]`    | The list of system services to start and enable.                                                              |
| `user_services`        | &#9989;  | `[]`    | The list of user services to start and enable.                                                                |
| `dconf_settings`       | &#9989;  | `[]`    | The list of dconf settings.<br><br>Each item in the list should be a dictionary containing `key` and `value`. |
| `kernel_install_limit` | &#9989;  | `3`     | The number of kernels to keep installed.                                                                      |

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: common
      vars:
        packages:
          - git
          - vim
          - wget
        flatpaks:
          - com.obsproject.Studio
          - com.spotify.Client
        services:
          - cockpit.socket
        user_services:
          - pipewire.socket
        dconf_settings:
          - key: /org/gnome/desktop/interface/clock-show-date
            value: "true"
          - key: /org/gnome/desktop/interface/clock-format
            value: "'12h'"
          - key: /org/gnome/desktop/datetime/automatic-timezone
            value: "true"
        kernel_install_limit: 3
```

License
-------

MIT

Author Information
------------------

Jared Hocutt (@jaredhocutt)
