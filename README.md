[![Build Status](https://travis-ci.org/chaosmail/ansible-roles-nodejs.svg?branch=master)](https://travis-ci.org/chaosmail/ansible-roles-nodejs)

Node.JS
=======

Ansible role to install nodejs, npm and global npm packages on CentOS or Ubuntu.

This role is tested via TravisCI on following platforms:
- Ubuntu 18.04 LTS (bionic)
- Ubuntu 16.04 LTS (xenial)
- Ubuntu 14.04 LTS (trusty)
- CentOS 7
- CentOS 6
- Debian 8 (Jessie)
- Debian 9 (Stretch)

This role is inspired by:
- https://github.com/geerlingguy/ansible-role-nodejs
- https://github.com/skandyla/ansible-role-nodejs

Requirements
------------

No requirements.

Role Variables
--------------

Set the Node.JS version via the `nodejs_version` property. Can be one of `"0.12", "4.x", "5.x", "6.x", "8.x", "10.x"`.

    nodejs_version: 10.x

Configure NPM packages that will be installed globally via the `npm_packages` property. Use format `[pkg1, pkg2, ..]` or `[{name: pkg1, version: 0.0.1}, {name: pkg2, version: 0.0.1}, ..]`.

    npm_packages:
      - http-server
      - typescript
      - webpack
      - less

Dependencies
------------

No dependencies.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: chaosmail.nodejs }

License
-------

MIT

Author Information
------------------

Christoph Koerner
