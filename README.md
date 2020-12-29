ansible-role-coturn
-------------------

[![Build Status](https://github.com/systemli/ansible-role-coturn/workflows/Integration/badge.svg?branch=master)](https://github.com/systemli/ansible-role-coturn/actions?query=workflow%3AIntegration)


Install coturn for Nextcloud like described here:
https://help.nextcloud.com/t/howto-setup-nextcloud-talk-with-turn-server/30794

This role might be useful in conjunction with [systemli.nextcloud](https://galaxy.ansible.com/systemli/nextcloud) or [systemli.jitsi_meet](https://galaxy.ansible.com/systemli/jitsi_meet).

Role Variables
--------------

see `defaults/main.yml`

Download
--------

Download latest release with `ansible-galaxy`

	ansible-galaxy install systemli.coturn


Testing & Development
---------------------

Tests
-----

For developing and testing the role we use Github Actions, Molecule, and Vagrant. On the local environment you can easily test the role with

Run local tests with:

```
molecule test
```

Requires Molecule, Vagrant and `python-vagrant, molecule-goss, molecule-vagrant` to be installed.For developing and testing the role we use Travis CI, Molecule and Vagrant. On the local environment you can easily test the role with


License
-------

GPLv3

Author Information
------------------

https://www.systemli.org
