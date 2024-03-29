![Ansible Lint](https://github.com/johanneskastl/ansible-role-install_SUSE_HA_packages/workflows/Ansible%20Lint/badge.svg)

install_SUSE_HA_packages
=========

Install packages related to the SUSE HA functionality. This includes removal of kernel-default-base, if it is installed it will be replaced by the "full" kernel-default.

Triggers a reboot after all of the updates were installed.

Requirements
------------

Machines must be registered in SCC and have the SUSE HA extensions enabled.

Role Variables
--------------

`suse_ha_packages`: List of packages to install. Override this if the default value does not fit for some reason:
```
suse_ha_packages:
  - pacemaker
  - pacemaker-cli
  - corosync
  - ha-cluster-bootstrap
  - yast2-iscsi-client
```

Dependencies
------------

Needs the [`johanneskastl.reboot`](https://github.com/johanneskastl/ansible-role-reboot) role to trigger a reboot after applying all updates.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: 'johanneskastl.install_SUSE_HA_packages'

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
