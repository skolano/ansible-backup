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

How to run backup
----------------
1. Download this repo `git clone https://github.com/skolano/ansible-backup`
2. Edit `/vars/main.yml`and configure your variables
3. Run playbook
```bash
ansible-playbook  playbook.yml
```
4. You can run this role on a schedule

`crontab -e`
```bash
# This scheduler will run Ansible playbook every day at 9:00 AM
0 9 * * * /usr/bin/ansible-playbook /path/to/your-playbook/playbook.yml
```


