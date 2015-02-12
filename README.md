Role Name
========

Install [Atlassian Confluence](https://www.atlassian.com/software/confluence)

Requirements
------------

A database, either PostgreSQL or MySQL, running somewhere.

Role Variables
--------------

All defined in defaults, so overrideable:

    confluence:
      version:   5.4.4
      baseurl:   http://www.atlassian.com/software/confluence/downloads/binary
      installer: atlassian-confluence-5.4.4.tar.gz
      user:      confluence
      # use postgresql or mysql
      dbconnector: postgresql
      packages:
        - java-1.7.0-openjdk
      tmp:       /var/tmp
      installto: /opt
      datadir:   /srv/confluence-data


Dependencies
------------


Example Playbook
-------------------------

    - hosts: confluence_servers
      roles:
         - { role: confluence }

License
-------

MIT/BSD

Author Information
------------------

Mark Phillips <mark@probably.co.uk>
http://probably.co.uk
