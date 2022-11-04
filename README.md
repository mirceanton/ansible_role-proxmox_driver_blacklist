Proxmox: Driver Blacklist
=========================

An Ansible role that configures the blacklisted drivers on a Proxmox VE host. 

Requirements
------------

N/A.

Role Variables
--------------

|          Variable          |     Type     |          Description          |
| :------------------------: | :----------: | :---------------------------: |
| `proxmox_driver_blacklist` | list(string) | List of drivers to blacklist. |

To check the default variables, take a look at the [defaults](defaults/main.yml) file.

Dependencies
------------

N/A.

Example Playbook
----------------

```yaml
- name: Blacklist nvidia drivers
  hosts: all

  roles:
    - role: mirceanton.proxmox_driver_blacklist
      vars:
        proxmox_driver_blacklist:
          - nvidia
          - nouveau
```

License
-------

MIT

Author Information
------------------

A role developed by [Mircea-Pavel ANTON](https://www.mirceanton.com).
