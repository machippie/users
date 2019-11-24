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
      - tboerger/homeshick-osx
    groups:
      - admin
    sshkeys:
      - ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAINaQYR0/Oj6k1H03kshz2J7rlGCaDSuaGPhhOs9FcZfn thomas@odin
```

### users_castles_force

Force castle updates

#### Default value

```YAML
users_castles_force: false
```

## Dependencies

None.

## License

Apache-2.0

## Author

Thomas Boerger
