Python Installer
================

Install python from source

Installation
------------

Add the following to your `requirements.yml`:

```yaml
roles:
  - name: thelonelyghost.python
    src: https://github.com/TheLonelyGhost/ansible-role-python
    version: master
```

Requirements
------------

- Requires the `community.general` collection be installed

Role Variables
--------------

| Name | Default | Description |
|:-----|:-------:|:------------|
| `python_download_url` | `https://www.python.org/ftp/python/{{ python_version }}/Python-{{ python_version }}.tgz` | URL from which Python release's source code is downloaded. Override this if in an air-gapped environment |
| `python_prefix` | `/usr/local` | Override this to (e.g.) `/usr` if your desired install location for python is `/usr/bin/python` |
| `python_version` | `3.9.0` | Change this to your desired version of python |


FYI, the following other variables are used in this role:

- `python_bin_dir`
- `python_bin`
- `python_executable_name`
- `python_version_major_minor`
- `python_system.dependencies`
- `python_system.extensions`

Dependencies
------------

- Requires the `community.general` collection be installed

Example Playbook
----------------

    - hosts: servers
      tasks:
        - import_role: thelonelyghost.python
          vars: 
          python_version: 2.7.15

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
