# Ansible playbook for Redmine

Ansible playbook for installing Redmine with plugins on CentOS/Ubuntu/Debian.

## Requirements

CentOS 7.6, Ubuntu 18.04 or Debian 10

## System

* Redmine 4.0.5
* PostgreSQL
* Apache
* Passenger

## Plugins

* Redmine WYSIWYG Editor plugin
* Redmine Mail From plugin
* Redmine Share plugin
* Redmine Local Avatars plugin
* Redmine XLSX Format Issue Exporter plugin
* Redmine View Customize plugin
* Redmine scm-creator plugin
* Redmine Banner plugin

## Installation

* Copy `hosts.sample` to `hosts` and edit `hosts`
* Copy `host_vars/localhost.yml.sample` to `host_vars/HOSTNAME.yml`
and edit the file as many as target hosts
* Run commend:
```
ansible-playbook -i hosts site.yml
```

## Notes

Enable configuration `allow_world_readable_tmpfiles`
if the playbook is executed by unprivileged user.

ansible.cfg:
```
[defaults]
allow_world_readable_tmpfiles = True
```

## License

MIT License

## Author

Takeshi Nakamura

(The original version is written by
[Far End Technologies Corporation](http://www.farend.co.jp/))
