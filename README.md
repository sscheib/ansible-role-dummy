dummy
=========
This is only a dummy role which I used for one of my blog posts. It does nothing useful.

Role Variables
--------------
| variable                                     | default                      | required | description                                                                    |
| :---------------------------------           | :--------------------------- | :------- | :----------------------------------------------------------------------------- |
| `message`                                    | `Hello World!`               | false    | This will be the message which is getting displayed                            |


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
    - role: 'dummy'
      vars:
        message: 'My personal message'
...
```

License
-------

GPL-2.0-or-later
