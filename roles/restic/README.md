Restic
======

Installs and configures restic.

Requirements
------------

- python >= 2.6
- python-dnf

Role Variables
--------------

| Variable       | Required | Default | Description                                                                                                                                                                                                                  |
| -------------- | -------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `restic_repos` | &#9989;  | `[]`    | A list of restic repos to target for backup and which files/directories to backup.<br><br>Each item in the list should be a dictionary containing `name`, `repo`, and `files`.<br.<br>See example playbook below for format. |

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: restic
      vars:
        restic_repos:
          - name: b2
            repo: "b2:bucketname:path/to/repo"
            env_vars:
              B2_ACCOUNT_ID: abcdef
              B2_ACCOUNT_KEY: ghijklm
              RESTIC_PASSWORD: password
            files:
              - /home/user1
              - /home/user2
```

License
-------

MIT

Author Information
------------------

Jared Hocutt (@jaredhocutt)
