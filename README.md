## Development Playbook

This is a playbook, and associated roles, which gives `SSH` access, `git` and `docker` with `docker-compose`. These 
few packages represent a very common subset of most development instances. 

### Designed for extension

While this playbook handles some common boilerplate dev tools, it will be much more useful when extended to your 
environment. 

### Usage

You will be required to create a `hosts` file and `group_vars` directory within the folder structure. You will also 
need to configure the roles by creating a `development.yml` file within the `group_vars` directory. The folder structure
will be as follows:

```
DevelopmentPlaybook/
├── group-vars/
│   └── development.yml
├── roles/
├── hosts
└── playbook.yml
```

You `development.yml` configures various options for the host. These options can be explored in the documentation within
the `roles` directory. A sample configuration will look something like:

```yml
---
ansible_ssh_user: root
os_user: "shaun"
git_username: "Shaun Egan"
git_email: "shaun@nonacreative.com"
git_coreeditor: "vim"
git_mergetool: "emerge"
ubuntu_version_name: "trusty"
```

Your `hosts` file represents the instances you want to provision as development environments and will look something 
like:

```
[development]
127.0.0.1
```

You will also require a `group_vars` directory for specifying some of the options built into the roles. The directory 
structure for this will be something like: