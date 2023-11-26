dummy
=========
This is only a dummy role which I used for one of my blog posts. It does nothing useful.

Role Variables
--------------
| variable                                     | default                      | required | description                                                                    |
| :---------------------------------           | :--------------------------- | :------- | :----------------------------------------------------------------------------- |
| `message`                                    | `Hello World!`               | false    | This will be the message which is getting displayed                            |

## Variable `pgi_packages`

An extended example of only the `pgi_packages` variable is illustrated down below:
```
pgi_packages:
  - name: 'qemu-guest-agent'
    state: 'latest'

  - name: 'openssh-server'
    state: 'present'

  - name: 'vim'
```
The only required option for a package is the `name`. The `state` can be either `latest`, to install the latest available version (so upgrade if it is already present), or `present`
to ensure that the package exists, which is also the default, if the `state` has not been defined.

Dependencies
------------

None

Example Playbook
----------------

```
---
- name: 'Install packages'
  hosts: 'all'
  gather_facts: false
  roles:
    - role: 'package_installation'
      vars:
        pgi_packages:
          - name: 'qemu-guest-agent'
            state: 'latest'

          - name: 'openssh-server'
            state: 'present'

          - name: 'vim'
...
```

License
-------

GPL-2.0-or-later
