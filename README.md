Role Name
=========

Backup role for Linux Desktop. Tasks:
- Create staging space for backup
- Create compressed archive for: network connections, hosts, data, flatpack apps, app configs etc...
  *You choose what you want to backup in the var file `vars/file/main.yml`*
- Export your backup data to backup destination (rclone remotes, mounted nfs or local folder)
- Clean staging space

Requirements
------------

- rclone (if you choose this method)

Role Variables
--------------

All variables are descibed in: `vars/file/main.yml`

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      roles:
         - { role: username.rolename, x: 42 }


Author Information
------------------
[Szymon Kolano](https://www.linkedin.com/in/skolano/)

