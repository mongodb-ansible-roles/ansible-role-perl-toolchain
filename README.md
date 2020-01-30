Ansible role for perl-toolchain
==================================

Installs the perl toolchain

[![GitHub Actions](https://github.com/mongodb-ansible-roles/ansible-role-perl-toolchain/workflows/Molecule%20Test/badge.svg)](https://github.com/mongodb-ansible-roles/ansible-role-perl-toolchain/actions?query=workflow%3A%22Molecule+Test%22)
[![GitHub Actions](https://github.com/mongodb-ansible-roles/ansible-role-perl-toolchain/workflows/Release/badge.svg)](https://github.com/mongodb-ansible-roles/ansible-role-perl-toolchain/actions?query=workflow%3A%22Molecule+Test%22)

Requirements
------------

None

Role Variables
--------------

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-------:|:--------:|
| `perl_toolchain_final_dest` | Location to install perl toolchain | string | `/opt/perl` | no |
| `perl_toolchain_sha` | Version of the perl toolchain to install | string | "ba92de2700c04ee2d4f82c3ffdfc33105140cb04" | no |
| `perl_toolchain_url` | URL of the perl toolchain to install | string | `https://s3.amazonaws.com/boxes.10gen.com/build/toolchain-drivers/mongo-perl-driver/perl-toolchain-{{ ansible_distribution | lower | replace('redhat', 'rhel') }}{{ ansible_distribution_version | replace('.', '') }}-{{ perl_toolchain_sha }}.tar.gz` | no |

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: ansible-role-perl-toolchain
```

License
-------

[Apache License](LICENSE)
