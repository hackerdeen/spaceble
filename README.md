# spaceble

Ansible for the hackerspace router

This repository is cloned on the router at /root/spaceble. To deploy changes:

    cd /root/spaceble
    git pull
    ansible-playbook playbook.yml

This was written in a hurry, the best way to ensure things are happening as they
should is to reboot the router after running the playbook.

## Disaster Recovery

Perform an installation of OpenBSD 6.6 with the following options:

* set up em0 -> dhcp
* start ssh by default
* switch console to com0
* speed 115200
* don't set up user
* allow root login
* timezone is Europe/London
* disk is sd0
* use whole disk mbr
* use autolayout
* install all sets

Once installation is complete, install git and ansible from packages.
