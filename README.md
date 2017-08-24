users
=========

This role creates and configures system users.

[![Build Status](https://travis-ci.org/plumelo/ansible-role-users.svg?branch=master)](https://travis-ci.org/plumelo/ansible-role-users)

Install
-------

ansible-galaxy install plumelo.users

Requirements
------------

This role requires Ansible 2.0 or higher and platform requirements are listed in the metadata file.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows. (For all variables, take a look at defaults/main.yml)

- name: "user"
    authorized:
      - "ssh-rsa AA... user@host"
    dotfiles:
      - file: '~/.bashrc'
        block: |
          export LC_ALL="en_US.UTF-8"
        marker: "#{mark} Language defaults"
    sudo: true

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
