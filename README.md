hyperized.patch
=========

Sometimes you need Ansible to patch Ansible when there's no recent release with your fix available.

Requirements
------------

Ansible 2.1 or above is highly recommended.

Role Variables
--------------

	ansible_patch_dir: /usr/local/lib/python2.7/dist-packages/ansible
	ansible_patch_dict: {}
	  # some_module:
	  #   file: some_module.py
	  #   path: modules/extras/some_module
	ansible_patch_user: root
	ansible_patch_group: staff
	ansible_patch_mode: 0644

Dependencies
------------

None

Example Playbook
----------------

Place the .py files you want to patch in /files, adjust ansible_patch_dict to match that pattern.

    - hosts: my_ansible_server
      become: yes
      roles:
         - { role: hyperized.patch }

License
-------

MIT

Author Information
------------------

Gerben Geijteman <gerben.geijteman@fdmediagroep.nl>
