[![Build Status](https://travis-ci.org/AAROC/UMD-role.svg?branch=master)](https://travis-ci.org/AAROC/UMD-role) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.825841.svg)](https://doi.org/10.5281/zenodo.825841)<!-- provide a detailed description of the issue -->

<!-- try to identify which service this issue is related to -->

# Logs and other information

<!-- please provide any relevant information from logs here
     Be sure to use the correct markdown formatting e.g.
    ```
       log
       output
    ```
-->



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

An example playbook can be seen in the [AAROC DevOps repo](https://github.com/AAROC/DevOps/blob/master/Ansible/top-bdiis.yml)

    - hosts: <umd_service>-servers
      roles:
         - { role: UMD-role, become: true, tags: "umd", umd_service: "emi-bdii-top", enable_umd: true, enable_preview: false, umd_version: 4 }


License
-------

Apache-2.0

Author Information
------------------

Bruce Becker brucellino@gmail.com
<a href="https://orcid.org/0000-0002-6607-7145" target="_blank" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon">orcid.org/0000-0002-6607-7145</a>

# Citing

Cite as

Bruce Becker. (2017, July 11). AAROC/UMD-role: Ansible role for UMD - v0.0.1. Zenodo. http://doi.org/10.5281/zenodo.825841
