postgresql\_install
===================

Installs PostgreSQL on EL 7 Linux.

Requirements
------------

* ssh access to your host
* the ability to sudo to root

Role Variables
--------------

* **postgres\_user** - Postgres user name, the first user role to be created in PostgreSQL
* **postgres\_user\_password** - PostgreSQL password for the above

Dependencies
------------

None.

Example Playbook
----------------


```yaml
# file: postgresql_install.yml
---
- name: Install PostgreSQL
  hosts: all
  gather_facts: no
  become: yes
  roles:
    - role: postgresql_install
      tags: [ postgresql, postgres ]
...
```

Example Usage
-------------

```cmd
ansible-playbook postgresql_install.yml -e "postgres_user=jdoe postgres_user_password=joe'sreallystrongpassword"
```

License
-------

BSD

Author Information
------------------

Written by V01dDweller in 2019.
