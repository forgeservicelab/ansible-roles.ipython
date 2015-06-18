IPython-spark
========

Notebook to install IPython and configure it for PySpark

Example playbook
----------------

```
---
- hosts: all
  sudo: True

  vars_prompt:
  - name: "ipython_pwd"
    prompt: "Please enter password for IPython"
    private: yes
    encrypt: "sha512_crypt"
    confirm: yes

  roles:
    - role: ipython-spark
      ipython_password: "{{ ipython_pwd }}"
```

License
-------

BSD

Author Information
------------------

FORGE Service Lab
