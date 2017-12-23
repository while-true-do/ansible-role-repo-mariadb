Empty space for build-links, logos or something like this.

# Ansible Role: Repo-MariaDB
| A role that installes yum repository for MariaDB from official [MariaDB Site](https://downloads.mariadb.org/mariadb/repositories/)

- It will create MariaDB.repo in /etc/yum.repos.d/
- It will import the rpm key from <https://yum.mariadb.org/RPM-GPG-KEY-MariaDB>
- If wtd_repo_mariadb_enabled is set to false it will remove the gpg-key and repository file

## Motivation

This role is needed to get a proper repo for newer MariaDB versions on CentOS 7.

## Installation

Install from [Ansible Galaxy](https://galaxy.ansible.com/while-true-do.repo-mariadb)

```
ansible-galaxy install while-true-do.repo-mariadb
```

Install from [Github](https://github.com/while-true-do/ansible-role-repo-mariadb)

```
git clone https://github.com/while-true-do/ansible-role-repo-mariadb.git while-true-do.repo-mariadb
```

## Requirements

**Used Modules**

-   [yum_repository](http://docs.ansible.com/ansible/latest/yum_repository_module.html)
-   [rpm_key](http://docs.ansible.com/ansible/latest/rpm_key_module.html)

## Role Variables
```yaml
# defaults/main.yml
wtd_repo_mariadb_enabled: True
wtd_repo_mariadb_version: '10.2'
```

## Dependencies

None.

## Example Playbook

Simple Example:

```yaml
- hosts: servers 
  roles:
    - { role: while-true-do.repo-mariadb }
```

## Testing

All tests should be put in [test directory](./tests/).

## Contribute / Bugs

Thank you so much for considering to contribute. Every contribution helps us.
We are really happy, when somebody is joining the hard work. Please have a look 
at the links first.

-   [Contribution Guidelines](./docs/CONTRIBUTING.md)
-   [Create an issue or Request](https://github.com/while-true-do/ansible-role-repo-mariadb/issues)
-   [See who was contributing already](https://github.com/while-true-do/ansible-role-repo-mariadb/graphs/contributors)

## License
This work is licensed under a [BSD License](https://opensource.org/licenses/BSD-3-Clause).

## Author Information

Blog: [blog.while-true-do.org](https://blog.while-true-do.org)

Mail: [hello@while-true-do.org](mailto:hello@while-true-do.org)
