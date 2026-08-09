url_file_handler
================
[![Ansible Lint](https://github.com/oxivanisher/role-spotify/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/oxivanisher/role-url_file_handler/actions/workflows/ansible-lint.yml)

Open .url files from Windows also on Linux in your default browser.

Role Variables
--------------

None.

Example Playbook
----------------
```yaml
- name: Configure .url file handler
  hosts: clients
  roles:
    - role: oxivanisher.linux_desktop.url_file_handler
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.linux_desktop](https://galaxy.ansible.com/ui/repo/published/oxivanisher/linux_desktop/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-linux_desktop).
