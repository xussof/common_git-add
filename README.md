common_git-add
=========

This role will add modified files inside a git repo.

Requirements
------------

All dependencies will appear on requirements.yml file

Role Variables
--------------
#EXAMPLE how to use it. DON'T UNCOMMENT
- name: Git add
  include_role:
    name: common_git-add
  vars:
    git_chdir: "/{{ host_root_dir }}/{{ repos_dir }}/{{ item.value.repo_git_name }}/{{ item.value.repo_project }}{{ item.value.repo_name }}"
    git_branch: "{{ item.value.repo_git_branch|default('master') }}"
    git_repo_name: "{{ item.value.repo_name }}"



Dependencies
------------

All dependencies will appear on requirements.yml file

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - common_git-add

TODO:
Working only with ssh not https yet

License
-------

BSD

Author Information
------------------
Made by @sergi-canas
