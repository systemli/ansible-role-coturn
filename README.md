ansible-role-coturn
-------------------

[![Build Status](https://github.com/systemli/ansible-role-coturn/workflows/Integration/badge.svg?branch=main)](https://github.com/systemli/ansible-role-coturn/actions?query=workflow%3AIntegration)


Install coturn for Nextcloud like described here:
https://help.nextcloud.com/t/howto-setup-nextcloud-talk-with-turn-server/30794

This role might be useful in conjunction with [systemli.nextcloud](https://galaxy.ansible.com/systemli/nextcloud) or [systemli.jitsi_meet](https://galaxy.ansible.com/systemli/jitsi_meet).

Role Variables
--------------

### Required Variables

The following variables are required (no defaults provided) and must always be
defined when using the role:

* `coturn_static_auth_secret`: Shared secret for client authentication. One way
  to generate an appropriate value is by using `pwgen -s 64 1`.
* `coturn_realm`: Use a syntactically correct hostname or domain.

### Optional Variables

See [defaults/main.yml](defaults/main.yml) for a list of optional variables.


Download
--------

Download latest release with `ansible-galaxy`

	ansible-galaxy install systemli.coturn


Testing & Development
---------------------

For developing and testing the role we use GitHub Actions and Molecule with the
Docker driver. The role supports Debian 12 (bookworm) and Debian 13 (trixie).
CI runs `molecule test` against both. Locally you need Docker or Podman,
`molecule`, `molecule-plugins[docker]` and `ansible-lint`. Run the test with

```
molecule test
```

The scenario uses Debian 13 by default; select another distribution with
`MOLECULE_DISTRO=debian12 molecule test`.

License
-------

GPLv3

Author Information
------------------

https://www.systemli.org
