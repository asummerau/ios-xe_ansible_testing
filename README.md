# Cisco IOS-XE Setup with Ansible

This GitHub repository demonstrates how to run a simple Ansible playbook.It provides an overview of the necessary components, commands for execution, and instructions for installing Ansible.

The directory contains the following files:

- `ansible.cfg`: Configuration file for Ansible settings, such as paths to Python interpreters.
- `hosts`: Inventory file that lists the managed nodes (e.g., network devices) and their connection details.
- `playbook.yml`: Ansible playbook file that contains the automation tasks to be executed on the managed nodes.

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
