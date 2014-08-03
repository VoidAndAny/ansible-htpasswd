# Ansible Htpasswd Role

[![Build Status](https://travis-ci.org/weareinteractive/ansible-role-htpasswd.png?branch=master)](https://travis-ci.org/weareinteractive/ansible-role-htpasswd)
[![Stories in Ready](https://badge.waffle.io/weareinteractive/ansible-role-htpasswd.svg?label=ready&title=Ready)](http://waffle.io/weareinteractive/ansible-role-htpasswd)

> `htpasswd` is an [ansible](http://www.ansible.com) role which: 
> 
> * installs `htpasswd`
> * manages `htpasswd` files

## Installation

Using `ansible-galaxy`:

```
$ ansible-galaxy install franklinkim.htpasswd
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):

```
$ arm install franklinkim.htpasswd
```

Using `git`:

```
$ git clone https://github.com/weareinteractive/ansible-role-htpasswd.git
```

## Variables

```
# htpasswd:
#   - name: myapp
#     users:
#       - { name: user, password: secret }

htpasswd: []
```

## Example playbook

```
- host: all
  roles: 
    - franklinkim.htpasswd
  vars:
    htpasswd:
      - name: myapp
        users:
        - { name: user, password: secret }
```

## Testing

```
$ git clone https://github.com/weareinteractive/ansible-role-htpasswd.git
$ cd ansible-role-htpasswd
$ vagrant up
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License
Copyright (c) We Are Interactive under the MIT license.