[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-docker-blue.svg?style=flat-square)](https://galaxy.ansible.com/xandout/random_name)

Random Name Generator
=========

This role will generate a random name similar to docker

Example Playbook
----------------

This role *does not* alter your system.  You will be able to use the random name by referencing `{{ random_name_full }}`

    ---
    - hosts: all
      roles:
        - { role: xandout.random_name}
      tasks:
        - name: Print name
          debug:
            msg: "{{ random_name_full }}"
