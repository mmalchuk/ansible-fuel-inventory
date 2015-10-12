Ansible inventory script for FUEL
---------------------------------
Translates FUEL nodes and roles to Ansible hosts and groups using FUEL python
client (rest API). Some FUEL related configuration data are also inserted as
fuel_\* variables.

As FUEL can have multiple environments configured, we expect environment
identifier is set as FUEL_ENV_ID environment variable otherwise the first
operational FUEL environment is used.

Some variables which can be used in playbooks:

    {{ fuel_network.management_vip }}
    {{ fuel_network.public_vip }}
    {{ fuel_master_ip }}
    {{ fuel_generated.rabbit.password }}
    {{ fuel_generated.mysql.root_password }}
    {{ fuel_generated.keystone.admin_token }}
    ...

References
----------
http://docs.ansible.com/intro_dynamic_inventory.html  
http://docs.ansible.com/developing_inventory.html  
https://github.com/stackforge/python-fuelclient
