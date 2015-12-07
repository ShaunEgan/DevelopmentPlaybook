Git
=========

Sets up git with global gitignore and configuration


Role Variables
--------------

The following variables are available to configure your git instance with:

* **git_os_user** - The username used to build the path for the user's home directory
* **git_username** - Standard git configuration username
* **git_email** -  Standard git configuration email
* **git_coreeditor** - Standard git configuration core editor
* **git_mergetool** - Standard git configuration merge tool

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      
      vars:
        - git_os_user: "bob"
          git_username: "Bob Belchers"
          git_email: "bob_belcher_555@email.com"
          git_coreeditor: "vim"
          git_mergetool: "emerge"
      
      roles:
         - git

License
-------

MIT

Author Information
------------------

Shaun Egan (shauneganza@gmail.com)
