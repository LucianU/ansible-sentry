sentry
======
- Installs system requirements
- Installs Sentry
- Creates superuser

Role Variables
--------------
| Variable | Description | Default value |
|----------|-------------|---------------|
|`sentry_conf`| Template for Sentry config file | `sentry.conf.py.j2` |
|`sentry_conf_dir`| Dir where Sentry config is installed | `/etc/sentry` |
|`sentry_socket`| Path to uWSGI socket serving the Sentry app | `/run/uwsgi/app/sentry/socket` |
|`sentry_system_packages`| System packages required by Sentry | See below |
|`sentry_user`| User running the Sentry app | `sentry` |
|`sentry_virtualenv`| Virtual env used by Sentry | `{{ python_virtualenvs_dir }}/sentry` |

`sentry_system_packages` values:
- libffi-dev
- libpq-dev
- libssl-dev
- libxslt1-dev
- libxml2-dev
- libyaml-dev
- python-setuptools

Dependencies
------------
- [python](https://github.com/LucianU/ansible-python)
- [postgres](https://github.com/LucianU/ansible-postgres)
- [nginx](https://github.com/LucianU/ansible-nginx)
- [uwsgi](https://github.com/LucianU/ansible-uwsgi)

License
-------
BSD
