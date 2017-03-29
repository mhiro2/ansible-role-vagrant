Ansible Role: vagrant
=======================

[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](https://github.com/mhiro2/ansible-role-vagrant/blob/master/LICENSE.txt)
[![Build Status](https://travis-ci.org/mhiro2/ansible-role-vagrant.svg?branch=master)](https://travis-ci.org/mhiro2/ansible-role-vagrant)

Install Vagrant and some plugins.

Requirements
------------

- Target: CentOS 7.x
- Ansible version: 2.0 or later

Role Variables
--------------

### Default role variables

```
arch: "{{ x86_64|default(ansible_architecture) }}"
vagrant_version: 1.9.3
vagrant_download_dir: /tmp
vagrant_package: "vagrant_{{ vagrant_version }}_{{ arch }}.rpm"
vagrant_package_url: "https://releases.hashicorp.com/vagrant/{{ vagrant_version }}/{{ vagrant_package }}"
vagrant_package_checksum: sha256:83e9da874398a113b7636f5a1fcf3f4c66120df6600b1b983267cb63162e85e1

vagrant_plugins:
  - sahara
  - vagrant-cachier
  - vagrant-hostmanager
  - vagrant-libvirt
  - vagrant-mutate
  - vagrant-share
```

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: mhiro2.vagrant, tags: ['vagrant'] }

License
-------

MIT

Author Information
------------------

[Masaaki Hirotsu](<mailto:hirotsu.masaaki@gmail.com>)
