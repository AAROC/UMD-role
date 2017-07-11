[![Build Status](https://travis-ci.org/AAROC/UMD-role.svg?branch=master)](https://travis-ci.org/AAROC/UMD-role)

Unified Middleware Distribution
=========

This Ansible role configures the host for the installation of [EGI Software products](http://repository.egi.eu/). These include the

  * [Unified Middleware Distribution](http://repository.egi.eu/category/umd_releases/distribution/)
  * [Cloud Middleware Distribution](http://repository.egi.eu/category/os-distribution/) for Open Stack.

The role configures the correct repositories and installs signing keys, as well as the middleware role you wish to add to the host.


Requirements
------------

None.

Role Variables
--------------

The `defaults.yml` accurately describes the default values.
There are no defaults set for the name of the middleware metapackage, since  it does not make sense to set a default for this.
If the `umd_service` variable is not set, the role will fail.

Dependencies
------------

No explicit dependencies.

Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: AAROC.umd, umd_service: top-bdii }

License
-------

Apache-2.0

Author Information
------------------

Bruce Becker brucellino@gmail.com
<a href="https://orcid.org/0000-0002-6607-7145" target="_blank" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon">orcid.org/0000-0002-6607-7145</a>
