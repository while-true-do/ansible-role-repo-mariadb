Empty space for build-links, logos or something like this.

# Ansible Role: Repo-MariaDB
| This role installes yum repository for MariaDB from official [MariaDB Site](https://downloads.mariadb.org/mariadb/repositories/)

- It will create MariaDB.repo under /etc/yum.repos.d
- It will import the rpm key from here [https://yum.mariadb.org/RPM-GPG-KEY-MariaDB]

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
CHANGEME
Special Packages, please inspect used modules to list the requirements here.
Please list all modules:

**Used Modules**

-   [yum_repository](http://docs.ansible.com/ansible/latest/yum_repository_module.html)
-   [rpm_key](http://docs.ansible.com/ansible/latest/rpm_key_module.html)

## Role Variables
CHANGEME
The variable files should be self-explanatary and pasted/linked here.
Explanation should be done **in** the files, if needed.
```yaml
# defaults/main.yml
wtd_repo_mariadb_version: '10.2'
```

```yaml
# vars/main.yml
bar: foo
```

## Dependencies
CHANGEME
Describe, if other roles are needed and link them here.

Dependency 1:

```
ansible-galaxy install -r requirements.yml
```

- vars

Dependency 2:

- link
- install
- vars

## Example Playbook
CHANGEME
Simple Example:

```yaml
- hosts: servers 
  roles:
    - { role: while-true-do.repo-mariadb }
```

Advanced Example:

```yaml
- hosts: servers 
  roles:
    - { role: while-true-do.repo-mariadb, foo: bar, bar: foo }
```

## Testing
CHANGEME
Describe, how the role can be tested.
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
