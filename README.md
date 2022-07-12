Role Name
=========

set sysctl values

Requirements
------------

Uses lihas_variables to merge the configuration from multiple sources

To run solo:

```
ansible-galaxy install -r requirements.yml
ansible-playbook -i localhost, sysctl.yml
```

Role Variables
--------------

Dictionaries with random name and entries `ctl` and `value`
### %.config.sysctl.SYSCTLSHORT.ctl
SYSCTLSHORT is just any identifiert, possibly giving a hint what we talk about
The name of the sysctl, e.g. net.ipv4.ip_forwarding
### %.config.sysctl.SYSCTLSHORT.value: 1
The value to set, e.g. 1

Dependencies
------------

* lihas_variables

Example Playbook
----------------

## Example Playbook
```
---
- hosts: '*'
  roles:
    - lihas_firewall
```

License
-------

GPL-3.0-or-later

Author Information
------------------

Adrian Reyer <lihas@lihas.de>

