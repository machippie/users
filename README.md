# users

[![Build Status](https://cloud.drone.io/api/badges/machippie/users/status.svg)](https://cloud.drone.io/machippie/users)

Ansible role to configure users

## Table of content

* [Default Variables](#default-variables)
  * [users](#users)
  * [users_castles_force](#users_castles_force)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

## Default Variables

### users

List of users to create

#### Default value

```YAML
users: []
```

#### Example usage

```YAML
users:
  - name: thomas
    primary_group: staff
    shell: /bin/bash
    castles:
      - tboerger/homeshick-base
      - name: tboerger/homeshick-osx
        force: True
    groups:
      - admin
    sshkeys:
      - ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAINaQYR0/Oj6k1H03kshz2J7rlGCaDSuaGPhhOs9FcZfn tboerger@host1
      - ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIC7oOi3qaDtfQVFhPKyd0Wk0C/y+QM71vtln8Rl44NlB tboerger@host2
      - ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIFcPTmdo+7eK+8n2yE7Kx1vyQ4yJwHBngvQOt1MPhKhR tboerger@host3
```

### users_castles_force

Force castle updates

#### Default value

```YAML
users_castles_force: true
```

## Dependencies

None.

## License

Apache-2.0

## Author

Thomas Boerger
