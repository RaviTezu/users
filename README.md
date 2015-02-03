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
    - hosts: servers_group
      roles:
         - users

License
-------
MIT

Author Information
------------------
Role created by RaviTezu - http://ravitezu.me
Date: Oct 22 2014

Warnings:
============
- If you are getting this error " one or more undefined variables: 'unicode object' has no attribute 'name' " please use the below format for vars/*.yml files:

groups_present.yml:
------------------
```
---
- 
  name: "group1" 
  state: present
  gid: 5000
```

- I have found that append is not working as expected. "append" option have "no" value by default, and it has to remove the user from all other groups apart from the groups mentioned in the user_present.yml file. In order to get it work, you have to define "groups: []" in the users_present.yml file explicitly. 
```
---
create_users:
-   
  name:  "rteja"
  gecos: "RaviTeja"
  groups: []
  pass:  "$6$xmlbExSxzxKxOxPxzxjxQxnZiUBW8TC8rxbxCxuxtxYxExNxExHxSxxxlrxx8xfxnxTxExrxYxAx.xIxn5xrxPx4xbx1"
  ssh_key: "rteja.pub"

```

Note: Feel free to mail me at ravi-teja@live.com or open a issue here for any help/issues. Have Fun! 
