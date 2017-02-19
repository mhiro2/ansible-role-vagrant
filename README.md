Ansible Role: vagrant
=======================

[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](https://github.com/mhiro2/ansible-role-vagrant/blob/master/LICENSE.txt)
[![Build Status](https://travis-ci.org/mhiro2/ansible-role-vagrant.svg?branch=master)](https://travis-ci.org/mhiro2/ansible-role-vagrant)

Install Vagrant and some plugins.

Plugins:
- sahara
- vagrant-cachier
- vagrant-hostmanager
- vagrant-libvirt
- vagrant-share

Requirements
------------

- Target: CentOS 7.x
- Ansible version: 2.0 or later

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: mhiro2.vagrant }

License
-------

MIT

Author Information
------------------

[Masaaki Hirotsu](<mailto:hirotsu.masaaki@gmail.com>)
