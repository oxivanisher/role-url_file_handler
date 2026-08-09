url_file_handler
================
[![Ansible Lint](https://github.com/oxivanisher/role-spotify/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/oxivanisher/role-url_file_handler/actions/workflows/ansible-lint.yml)

Open .url files from Windows also on Linux in your default browser.

Role Variables
--------------

| Name                          | Comment                                                                                   | Default value                                   |
| ----------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------- |
| url_file_handler_mimetype     | MIME type used to identify Windows .url (Internet Shortcut) files                         | `application/x-mswinurl`                        |
| url_file_handler_script_path  | Where the opener script gets installed                                                    | `/usr/local/bin/open-url-file.sh`               |
| url_file_handler_desktop_file | Desktop entry that wraps the script for the file-manager/xdg-open layer                   | `/usr/share/applications/open-url-file.desktop` |
| url_file_handler_mime_package | Shared-mime-info package defining the mimetype+glob                                       | `/usr/share/mime/packages/x-mswinurl.xml`       |
| url_file_handler_use_notify   | Emit a desktop notification when a .url file has no URL= line instead of failing silently | `true`                                          |
| url_file_handler_os_users     | Users for which the mime-type will be applied                                             | `[]`                                            |

Note: The shared-mime-info package defining the mimetype+glob is harmless even if the distro already ships this type; ours simply reasserts it.

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
