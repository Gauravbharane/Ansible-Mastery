# Ansible-Mastery
Ansible Mastery series

# Ansible-Mastery

Welcome to the Ansible Mastery series! This repository is dedicated to providing a comprehensive guide to mastering Ansible, an open-source automation tool.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [Folder Structure](#folder-structure)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Ansible is a powerful automation tool that allows you to manage and configure systems, deploy software, and orchestrate complex tasks. This repository aims to provide tutorials, examples, and best practices for using Ansible effectively.

## Installation

To install Ansible, follow these steps:

1. **Using pip (Python package manager):**
    ```bash
    pip install ansible
    ```

2. **Using a package manager:**

    - **Debian/Ubuntu:**
      ```bash
      sudo apt update
      sudo apt install ansible
      ```

    - **RHEL/CentOS:**
      ```bash
      sudo yum install ansible
      ```

For more detailed installation instructions, refer to the [official Ansible documentation](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

## Getting Started

To get started with Ansible, create an inventory file and a simple playbook.

1. **Create an inventory file:**
    ```ini
    [servers]
    server1 ansible_host=192.168.1.1
    server2 ansible_host=192.168.1.2
    ```

2. **Create a playbook:**
    ```yaml
    - name: Example Playbook
      hosts: servers
      tasks:
        - name: Ensure Nginx is installed
          apt:
            name: nginx
            state: present
    ```

3. **Run the playbook:**
    ```bash
    ansible-playbook -i inventory playbook.yml
    ```

## Folder Structure

The repository is organized as follows:
Ansible-Mastery/ 
├── Ansible_batch/ 
│ ├── playbooks/
│ ├── roles/
│ └── inventory/
├── LICENSE
├── README.md
└── examples/
├── example1.yml
└── example2.yml


- **Ansible_batch/**: Contains batch scripts, playbooks, roles, and inventory files.
- **examples/**: Contains example playbooks demonstrating various Ansible functionalities.

## Configuration

Here is an example `ansible.cfg` file for configuring Ansible:

```ini
[defaults]
inventory= ./inventory
roles_path= ./roles
collections_path= ./mycollections:~/.ansible/collections:/usr/share/ansible/collections
remote_user= root
ask_pass= false

[privilege_escalation]
become= true
become_method= sudo
become_user= root
become_ask_pass= false

```
- **Ansible_batch/**: Contains batch scripts, playbooks, roles, and inventory files.
- **examples/**: Contains example playbooks demonstrating various Ansible functionalities.

## Contributing

We welcome contributions to the Ansible Mastery series! To contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a new Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.



