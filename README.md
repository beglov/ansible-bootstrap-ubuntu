# Initial Server Setup on Ubuntu

This playbook will execute a initial server setup for Ubuntu systems.

The included tasks are following:

* Create a new regular user with sudo privileges
* Set authorized key for remote user
* Disable password authentication for root
* Update apt and install required system packages
* Configure and enable UFW

## Running this Playbook

### 0. Requirements

First of all, install the latest version of Ansible, in Ubuntu:

```bash
sudo apt-add-repository ppa:ansible/ansible
sudo apt update
sudo apt install ansible
```

### 1. Obtain the playbook

```bash
git clone https://github.com/beglov/ansible-bootstrap-ubuntu.git
cd ansible-bootstrap-ubuntu
```

### 2. Add your remote server’s IP to inventory file

```bash
cp hosts.sample hosts
nano hosts
```

### 3. Run the Playbook

```bash
ansible-playbook bootstrap.yml -i hosts -l [target] -u [remote user]
```
