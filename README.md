Docker role
=========

install docker

Requirements
------------

Host accesible via SSH with password

Role Variables
--------------

any so far

Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
---
- name: "nginx gitted"
  hosts: centos01
  vars_files:
  - "/home/ubuntu/secret.yaml"
  roles:
    - docker_role
  tasks:
    - name: Git checkout
      ansible.builtin.git:
        repo: 'https://github.com/diranetafen/static-website-example.git'
        dest: /var/www/html
        force: yes

    - name: Restart a container
      docker_container:
        name: nginx-dimension
        image: nginx
        state: started
        restart: yes
        ports:
         - "80:80"
        volumes:
         - /var/www/html/:/usr/share/nginx/html/

```

License
-------

opensource take it sell it idc

Author Information
------------------

Fahim devops to be
