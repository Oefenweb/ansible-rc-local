## rc-local

[![Build Status](https://travis-ci.org/Oefenweb/ansible-rc-local.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-rc-local) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-rc--local-blue.svg)](https://galaxy.ansible.com/Oefenweb/rc-local)

Manages rc.local in Debian-like systems.

#### Requirements

None

#### Variables

None

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
```

#### License

MIT

#### Author Information

* Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-rc-local/issues)!
