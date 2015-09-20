Rubedo
======
[![Travis branch](https://img.shields.io/travis/GMaissa/ansible-role-rubedo/master.svg)](https://travis-ci.org/GMaissa/ansible-role-rubedo)

This Ansible role installs [Rubedo](http://www.rubedo-project.org) andd all it dependencies

Requirements
------------

No external requirements exist to this role.

Role Variables
--------------

Apache virtualhost configuration:

    # Rubedo vhost configuration
    rubedo_vhost:
      filename: rubedo.conf
      enabled: yes
      listen: '*:80'
      root: /var/www/rubedo
      name: rubedo.local
      aliases:
        - www.rubedo.local

PHP configuration:

    # Define php timezone
    rubedo_php_date_timezone: Europe/Paris

    # Define APC shm size
    rubedo_php_apc_shm_size: 128M

Rubedo sources download configuration:

    # Download Rubedo sources
    rubedo_download: false

    # Rubedo version to download
    rubedo_version: 3.2.0


License
-------

BSD

Author Information
------------------

Guillaume Maïssa <pro.g@maissa.fr>
