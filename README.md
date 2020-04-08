ansible-role-coturn
-------------------
[![Build Status](https://travis-ci.com/systemli/ansible-role-coturn.svg?branch=master)](https://travis-ci.com/systemli/ansible-role-coturn) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-coturn-blue.svg)](https://galaxy.ansible.com/systemli/coturn/)

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

Tests
-----

For developing and testing the role we use Travis CI, Molecule and Vagrant. On the local environment you can easily test the role with

```
pip install molecule-vagrant ansible-lint
molecule test
```

This requires [Vagrant](https://www.vagrantup.com/downloads.html) to be installed.

License
-------

GPLv3

Author Information
------------------

https://www.systemli.org
