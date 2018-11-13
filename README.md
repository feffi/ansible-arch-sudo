# ansible-arch-sudo

Ansible role to manage sudo and sudoers file.

[![Build Status](https://img.shields.io/travis/feffi/ansible-arch-sudo.svg)](https://travis-ci.org/feffi/ansible-arch-sudo) [![Github All Releases](https://img.shields.io/github/downloads/feffi/ansible-arch-sudo/total.svg)](https://github.com/feffi/ansible-arch-sudo) [![GitHub forks](https://img.shields.io/github/forks/feffi/ansible-arch-sudo.svg?style=social&label=Fork)](https://github.com/feffi/ansible-arch-sudo) [![GitHub stars](https://img.shields.io/github/stars/feffi/ansible-arch-sudo.svg?style=social&label=Star)](https://github.com/feffi/ansible-arch-sudo) [![GitHub watchers](https://img.shields.io/github/watchers/feffi/ansible-arch-sudo.svg?style=social&label=Watch)](https://github.com/feffi/ansible-arch-sudo) [![Twitter Follow](https://img.shields.io/twitter/follow/feffi1.svg?style=social&label=Follow)](https://twitter.com/feffi1) [![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/feffi/ansible-arch-sudo/blob/master/LICENSE)
## Requirements

- Ansible 2.7.1
- pacman ;-)

### ansible.cfg

```yaml
hash_behaviour = merge
```

## Install

Just add the role to your ``requirements.yml`` file:

```yaml
- src: https://github.com/feffi/ansible-arch-sudo.git
  name: ansible-arch-sudo
```

## Role Defaults Variables

```yaml
ansible_arch_sudo: {
  # Users to add to sudoers
  users: [],
  # Groups to add to sudoers
  groups: [
    "wheel"
  ]
}
```

Example:

```yaml
- hosts: all
  vars:
    ansible_arch_sudo:
      users: []
      groups:
        - "wheel"
  roles:
    - { role: ansible-arch-sudo }
```
