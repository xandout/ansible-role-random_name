[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-xandout.random_name-blue.svg?style=flat-square)](https://galaxy.ansible.com/xandout/random_name)

Random Name Generator
=========

This role will generate a random name similar to docker

Role Variables
--------------


    random_name_seperator: Default is `_`, if set to `-` then the result will be a compliant hostname


Example Playbook
----------------

This role *does not* alter your system.  You will be able to use the random name by referencing `{{ random_name_full }}`

    # This will produce names like docker
    ---
    - hosts: all
      roles:
        - { role: xandout.random_name}
      tasks:
        - name: Print name
          debug:
            msg: "{{ random_name_full }}"

    # This will produce valid hostnames
    ---
    - hosts: all
      roles:
        - { role: xandout.random_name, random_name_seperator: "-"}
      tasks:
        - name: Print name
          debug:
            msg: "{{ random_name_full }}"
