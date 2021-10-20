ansible-role-coturn
-------------------

[![Build Status](https://github.com/systemli/ansible-role-coturn/workflows/Integration/badge.svg?branch=master)](https://github.com/systemli/ansible-role-coturn/actions?query=workflow%3AIntegration)


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

For developing and testing the role we use Github Actions, Molecule, and Vagrant. On the local environment you can easily test the role with

```
molecule test
```

License
-------

GPLv3

Author Information
------------------

https://www.systemli.org
