users
=========

This role creates and configures system users.

[![Build Status](https://travis-ci.org/plumelo/ansible-role-users.svg?branch=master)](https://travis-ci.org/plumelo/ansible-role-users)

Requirements
------------

This role requires Ansible 2.0 or higher and platform requirements are listed in the metadata file.

Install
-------

```sh
ansible-galaxy install plumelo.users
```

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows.
For all variables, take a look at [defaults/main.yml](https://github.com/plumelo/ansible-role-users/blob/master/defaults/main.yml)

```yaml
# when we make a new user automatically make the user group
  users_group_per_user: yes

# choose the user shell(bash,zsh,fish,etc)
  users_shell: /bin/bash

# multiple users
  users_users: []
```
Example Playbook
----------------
```yaml
Install role plumelo.users

    - hosts: servers
      roles:
         - role: plumelo.users

And make a new user

    name: "user"
      authorized:
        - "ssh-rsa AA...user@domain"
      dotfiles:
        - file: '~/.bashrc'
          block: |
            export LC_ALL="en_US.UTF-8"
          marker: "#{mark} Language defaults"
      sudo: true
```
  Dependencies
  ------------

None

License
-------

BSD

Author Information
------------------

- plumelo.com
