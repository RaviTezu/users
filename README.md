Users:
=========

This role manages user accounts and groups on a server.
*Please see Warnings section below*

Role Variables
--------------
- For creating new groups - groups_present.yml 
- For deleting groups - groups_absent.yml
- For creating new users - users_present.yml
- For deleting users - users_absent.yml
- vars:
    - create_groups
    - delete_groups
    - create_users 
    - delete_users

Example Playbook
----------------
    - hosts: servers
      roles:
         - users

License
-------
MIT

Author Information
------------------
Role created by RaviTezu 
Date: Oct 22 2014

Warning:
============
If you are getting this error " one or more undefined variables: 'unicode object' has no attribute 'name' " please use the below format for vars/*.yml files:

groups_present.yml:
------------------
```
---
vars file for users
- 
  name: "group1" 
  state: present
  gid: 5000
```
