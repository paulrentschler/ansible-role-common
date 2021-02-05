paulrentschler.common
=====================

[![MIT licensed][mit-badge]][mit-link]

Installs and configures software for all Ubuntu Linux machines.

Requirements
------------

None.


Role Variables
--------------

The following variables are available with defaults defined in `defaults/main.yml`:

Specify if a custom scripts directory (`/usr/local/scripts`) should be created

    common_scripts_directory: yes

Specify the owner and group for the scripts directory, if created:

    common_scripts_owner: "{{ devops_user|default(ansible_user) }}"
    common_scripts_group: "devops"


Dependencies
------------

None.


Example Playbook
----------------

Simple version that creates the scripts directory:

    - hosts: all
      roles:
         - paulrentschler.common


Install the software but do **not** create the scripts directory:
    - hosts: all
      roles:
        - { role: paulrentschler.common,
            common_scripts_directory: no
            }


License
-------

[MIT][mit-link]


Author Information
------------------

Created by Paul Rentschler in 2021.


[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://github.com/paulrentschler/ansible-role-common/blob/master/LICENSE
