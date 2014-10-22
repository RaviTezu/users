Users:
=========

This role manages user accounts and groups on a server.

Role Variables
--------------
- For creating new groups - groups_present.yml 
- For detelet groups - groups_absent.yml
- For creating new users - users_present.yml
- For detelet users - users_absent.yml
- vars:
    - create_groups
    - delete_groups
    - create_users 
    - delete_users

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

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
