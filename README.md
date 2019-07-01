# Ansible Role: Install awscli

[![Build Status](https://travis-ci.org/tschifftner/ansible-role-awscli.svg?branch=master)](https://travis-ci.org/tschifftner/ansible-role-awscli)

Installs awscli from source on Debian/Ubuntu linux servers.

## Requirements

ansible 2.0+

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
awscli_profiles:
  - user: jenkins
    profiles:
      - name: testing
        aws_access_key_id: '<testing access key>'
        aws_secret_access_key: '<testing secret key>'
```

## Dependencies

None.

## Installation

```
$ ansible-galaxy install tschifftner.awscli
```

## Example Playbook

    - hosts: server
    
      vars:
        awscli_profiles:
          - user: jenkins
            profiles:
              - name: testing
                aws_access_key_id: '<testing access key>'
                aws_secret_access_key: '<testing secret key>'

      roles:
        - { role: tschifftner.awscli }

## Supported OS

 - Debian 10 (Buster)
 - Debian 9 (Stretch)
 - Debian 8 (Jessie)
 - Ubuntu 18.04 (Bionic Beaver)
 - Ubuntu 16.04 (Xenial Xerus)
 
## Required ansible version

Ansible 2.5+

## License

[MIT License](http://choosealicense.com/licenses/mit/)

## Author Information

 - [Tobias Schifftner](https://twitter.com/tschifftner), [ambimax® GmbH](https://www.ambimax.de)