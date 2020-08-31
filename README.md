[![Build Status](https://travis-ci.com/BenoitCharret/certbot.svg?branch=master)](https://travis-ci.com/BenoitCharret/certbot)

Role Name
=========

This role install a let's encrypt certiticate as the default certificate and using a dns validation against OVH.
During the installation, the role will generate the certificate and install a cron to easily renew it.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

 name | description
 --- | ---
 dns_ovh_endpoint | OVH Endpoint 
 dns_ovh_application_key | OVH application key
 dns_ovh_application_secret |  OVH application secret
 dns_ovh_consumer_key | OVH consumer key
 python_path | the path for the directory of python (maybe /volume1/@appstore/py3k/usr/local/bin/ if python is installed with synology package manager
 dns_email | the mail that will receive information and reminder from let's encrypt
 dns_domain | the domain for which the certificate will be generated (may be a wildcard certificate
    
 The OVH credentials can be created through this url : https://eu.api.ovh.com/createApp/

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
         
     - hosts: all
       become: true
       roles:
         - benoitcharret.certbot

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
