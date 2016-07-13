# Ansible Role: Install awscli

[![Build Status](https://travis-ci.org/tschifftner/ansible-role-awscli.svg)](https://travis-ci.org/tschifftner/ansible-role-awscli)

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
Ansible          | Debian Jessie    | Ubuntu 14.04
:--------------: | :--------------: | :-------------:
2.0              | Yes              | Yes
2.1              | Yes              | Yes

## License

MIT / BSD

## Author Information

 - [Tobias Schifftner](https://twitter.com/tschifftner), [ambimax® GmbH](https://www.ambimax.de)