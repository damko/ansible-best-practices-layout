# Ansible best practices : Alternative layout


This is a lazy way to get [Ansible Directory Layout](https://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html#directory-layout) configured.

Simply clone this repo, remove `.git` and start working on your ansible project.

This is what you get:

``` bash
> tree -a

|
├── filter_plugins
├── group_vars
│   ├── atlanta.yml
├── host_vars
│   └── .gitignore
├── library
│   └── .gitignore
├── module_utils
│   └── .gitignore
├── production              # production inventory file
├── README.md
├── roles
│   └── common
│       ├── defaults
│       │   └── main.yml
│       ├── files
│       │   └── .gitignore
│       ├── handlers
│       │   └── main.yml
│       ├── library
│       │   └── .gitignore
│       ├── lookup_plugins
│       │   └── .gitignore
│       ├── meta
│       │   └── main.yml
│       ├── module_utils
│       │   └── .gitignore
│       ├── tasks
│       │   └── main.yml
│       ├── templates
│       │   └── .gitignore
│       └── vars
│           └── main.yml
├── site.yml
└── staging                 # staging inventory file
```

Run the main playbook:

``` bash
ansible-playbook -i production site.yml
```

or
``` bash
ansible-playbook -i staging site.yml
```