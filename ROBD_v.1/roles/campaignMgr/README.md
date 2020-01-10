Role Name
=========

Role for campaign manager new feature deployment which includes db backup and fetch db to local machine.
Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Set the db vars accordingly.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

OMMAND for syntax validation:
------------------------------
ansible-playbook -i hosts cm_site.yml --syntax-check --ask-vault-pass

Command to Execute:
------------------
ansible-playbook -i hosts cm_site.yml  --ask-vault-pass

Encryption done on vars/main.yml:

[root@os7 campaignMgr]# ansible-vault view vars/main.yml 
Vault password: 
---
# vars file for campaignMgr
exclude_db:
 - Database
 - information_schema
 - performance_schema
 - mysql
 - cm_6_0_4_0
 - cam3
 - gprs_offer
 - mca
 - pkg_dpi_integration
 - robd_3_2_5
 - service_activator
 - test
 - testmodule

vault_root_passwd: onmobile

License
-------

BSD

Author Information
------------------
Partha Pradhan
