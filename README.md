install_SUSE_HA_packages
=========

Install packages related to the SUSE HA functionality 

Requirements
------------

Machines must be registered in SCC and have the SUSE HA extensions enabled.

Role Variables
--------------

`suse_ha_packages`: List of packages to install.

Dependencies
------------

Needs the reboot role to trigger a reboot after applying all updates.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: johanneskastl.install_SUSE_HA_packages, x: 42 }

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
