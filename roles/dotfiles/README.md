Dotfiles
=========

Installs dotfiles repository and enables the specified sets of dotfiles.

Requirements
------------

- git >= 1.7.1
- python >= 2.6
- python-dnf

Role Variables
--------------

| Variable           | Required | Default | Description                                                                                                        |
| ------------------ | -------- | ------- | ------------------------------------------------------------------------------------------------------------------ |
| `dotfiles_enabled` | &#9989;  | `[]]`   | A list of dotfiles to enable.<br><br>Each item in the list should be a dictionary containing `name` and `dotfile`. |

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: dotfiles
      vars:
        dotfiles_enabled:
          - name: git
            dotfile: ~/.gitconfig
          - name: vim
            dotfile: ~/.vimrc
          - name: zsh
            dotfile: ~/.zshrc
```

License
-------

MIT

Author Information
------------------

Jared Hocutt (@jaredhocutt)
