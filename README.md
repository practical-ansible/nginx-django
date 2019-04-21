### Variables

[![CircleCI](https://img.shields.io/circleci/project/github/practical-ansible/nginx-django.svg)](https://circleci.com/gh/practical-ansible/nginx-django)
[![Quality](https://img.shields.io/ansible/quality/21430.svg)](https://galaxy.ansible.com/practical-ansible/nginx-django)
[![Downloads](https://img.shields.io/ansible/role/d/21430.svg)](https://galaxy.ansible.com/practical-ansible/nginx-django)

#### Project archive

This role expects you to bundle your django application into archive. We recommend to use [setuptools](https://pypi.python.org/pypi/setuptools) as it is widely used, but a simple zip archive should work as well. Set `django_archive` to path of your archive.

#### Project environment

`django_project_environment` is used to deploy multiple environments on same host, which can be useful, when you're running lowcost. Defaults to "staging".

#### Project name

Set `django_project_name` to your project name. Looks for environment variable `DJANGO_PROJECT_NAME` by default.

#### Project version

Set `django_project_version` to your project version. Defaults to "develop". Deploying same version twice will overwrite what is on the server. Old versions are stored on the server, so it is easy to quickly fall back just by changing the symlink.

#### Server name

Set `django_server_name` to domain name of your project. Separate by space to use multiple names. Looks for environment variable `DJANGO_SERVER_NAME` by default.

#### Server django projects directory

Set `django_projects_directory` to path where you usually store django projects. Defaults to "/var/www".

#### Static files directory

Set `django_static_dir` to directory where you store static files. Defaults to empty string. We recommend storing static files externally on CDN, for example AWS S3. Looks for environment variable `DJANGO_STATIC_DIR` by default.

#### Django configuration module

Set `django_config` to module path of your Django configuration. For example: 'app.settings'.

#### Extra django configuration template

Set `django_config_file` to path of external configuration template of your django application.

#### Django wsgi file

Set `django_file_file` to path of wsgi file of your django application.
