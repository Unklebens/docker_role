Docker role
=========

install docker

Requirements
------------

none

Role Variables
--------------

any so far

Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- hosts: centos01:worker03
  become: true
  vars_files:
    - secret.yaml
  roles:
    - docker_role


License
-------

opensource take it sell it idc

Author Information
------------------

Fahim devops to be
