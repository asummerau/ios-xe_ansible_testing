# Cisco IOS-XE Setup with Ansible

This directory contains the following files:

- ansible.cfg
- hosts
- playbook.yml

## Installation 

Create a Python virtual environment and install all necessary libraries:

```bash
python3 -m venv env
source env/bin/activate
(env) pip3 install ansible
(env) pip3 install paramiko
```

Verify the installation by checking the version of Ansible:

```bash
(env) ansible --version
```

Update Path to your Python interpeter into your ansible.cfg file

```bash
(env) echo "interpreter_python=$(which python)" >> ansible.cfg
```

Execute the Ansible Playbook

```bash
(env) ansible-playbook -i hosts playbook.yml
```

To exit the virtual environment use:

```bash
(env) deactivate
```
