## Common tasks to setup a VM for a project

### About this

I usually develop apps in NodeJs or Golang when deploying the app for development and testing I setup a VM (VPS) for that.
So I thought it would be nice to it automated.
Feel free to to add your tasks too, all PRs are welcomed!.
If you don't want a task you can just comment it out in the [playbook.yml](./playbook.yml) file.

### Requirements
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
- VM with SSH access

### How to use
- Clone this repo
```bash
git clone
```

- Edit the [playbook.yml](./playbook.yml) file to your needs

- Edit the [inventory/host_vars/server-1.yml](./inventory/host_vars/server-1.yml) with your VM IP.

- Edit the [inventory/group_vars/web.yml](./inventory/group_vars/web.yml) with your VM ssh user and local keys.

- Run the playbook

```bash
ansible-playbook playbook.yml -i inventory
```