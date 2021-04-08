## rc-local

[![CI](https://github.com/Oefenweb/ansible-sysfs/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-sysfs/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-rc--local-blue.svg)](https://galaxy.ansible.com/Oefenweb/rc_local)

Manages rc.local in Debian-like systems.

#### Requirements

None

#### Variables

* `rc_local_commands`: [default: `[]`]: Commands to add to `rc.local`

#### Dependencies

None

#### Example

##### Simple

```yaml
---
- hosts: all
  roles:
    - rc-local
```

##### Advanced

```yaml
---
- hosts: all
  roles:
    - rc-local
  vars:
    rc_local_commands:
      - |
          # transparen hugepage
          if test -f /sys/kernel/mm/transparent_hugepage/enabled; then
            echo never > /sys/kernel/mm/transparent_hugepage/enabled;
          fi
          if test -f /sys/kernel/mm/transparent_hugepage/defrag; then
            echo never > /sys/kernel/mm/transparent_hugepage/defrag;
          fi
      - |
          # something else
```

#### License

MIT

#### Author Information

* Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-rc-local/issues)!
