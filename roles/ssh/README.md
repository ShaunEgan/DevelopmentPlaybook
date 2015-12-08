SSH
=========

Adds a user to the host and installs a public key for that user

Requirements
------------

SSH

Role Variables
--------------

The following variables are available to configure your ssh instance with:

* **os_user** - The username used to build the path for the user's home directory
* **os_user_public_key** - The path to the public key to use, default is `~/.ssh/id_rsa.pub` 

Example Playbook
----------------

    - hosts: servers
          
          vars:
            os_user: "bob"
            os_user_public_key: "~/repositories/keys/my-key.pub"
          
          roles:
             - ssh

License
-------

MIT

Author Information
------------------

Shaun Egan (shauneganza@gmail.com)
