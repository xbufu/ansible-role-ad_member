Ansible Role: Domain Member
=========

An Ansible role to join a new machine to AD domain.

Requirements
------------

None.

Role Variables
--------------

```yml
domain_pdc: pdc01
domain_name: ad01.bufu-sec.com
domain_admin_user: 'ad01\administrator'
domain_admin_password: Password!
domain_ou_path: 'DC=ad01,DC=bufu-sec,DC=com'
domain_computer_name: '{{ ansible_facts.hostname }}'
```

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: wks01
  roles:
    - role: xbufu.ad_member
      vars:
        domain_pdc: pdc01
        domain_name: ad01.bufu-sec.com
        domain_admin_user: 'ad01\administrator'
        domain_admin_password: Password!
        domain_ou_path: 'DC=ad01,DC=bufu-sec,DC=com'
        domain_computer_name: '{{ ansible_facts.hostname }}'
```

License
-------

MIT / BSD

Author Information
------------------

Created by xbufu.
