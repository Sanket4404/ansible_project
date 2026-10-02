# Ansible Automation Project

A practical Ansible project focused on **configuration management, inventory-driven automation, SSH-based remote execution, and repeatable Linux server administration**.

This repository is part of my broader DevOps learning portfolio alongside Terraform, Docker, Kubernetes, AWS, and CI/CD.

## 🎯 Project Objectives

* Understand Ansible control-node architecture
* Manage remote Linux systems through SSH
* Create reusable playbooks
* Organize automation through inventory
* Reduce repetitive server administration
* Practice idempotent configuration management
* Troubleshoot automation failures

## 🏗️ Ansible Architecture

```text
                 Developer / Operator
                         │
                         ▼
                ┌─────────────────┐
                │ Ansible Control │
                │      Node       │
                └────────┬────────┘
                         │
                      SSH
                         │
          ┌──────────────┼──────────────┐
          ▼              ▼              ▼
       Server 1       Server 2       Server 3
```

Ansible uses an agentless model, with remote systems managed primarily through SSH.

## 📁 Repository Structure

```text
ansible_project/
├── playbooks/
└── README.md
```

The `playbooks/` directory contains the automation logic.

## 🧰 Technology Stack

| Area            | Technology        |
| --------------- | ----------------- |
| Automation      | Ansible           |
| Configuration   | YAML              |
| Remote Access   | SSH               |
| Managed Systems | Linux             |
| Inventory       | Ansible Inventory |
| Environment     | AWS / Linux Lab   |
| Version Control | Git               |

## 🚀 Getting Started

Verify Ansible:

```bash
ansible --version
```

Test connectivity:

```bash
ansible all -i <inventory-file> -m ping
```

## ▶️ Run a Playbook

```bash
ansible-playbook \
  -i <inventory-file> \
  playbooks/<playbook>.yml
```

Verbose execution:

```bash
ansible-playbook \
  -i <inventory-file> \
  playbooks/<playbook>.yml \
  -v
```

## 🔍 Useful Commands

View inventory:

```bash
ansible-inventory \
  -i <inventory-file> \
  --graph
```

Test all hosts:

```bash
ansible all \
  -i <inventory-file> \
  -m ping
```

Gather system facts:

```bash
ansible all \
  -i <inventory-file> \
  -m setup
```

Execute a remote command:

```bash
ansible all \
  -i <inventory-file> \
  -m command \
  -a "uname -a"
```

## 🧠 Why Ansible?

Without automation:

```text
SSH → Install package → Configure → Restart
SSH → Install package → Configure → Restart
SSH → Install package → Configure → Restart
```

With Ansible:

```text
                 Playbook
                    │
          ┌─────────┼─────────┐
          ▼         ▼         ▼
       Server 1  Server 2  Server 3
```

The desired configuration is defined once and can be applied consistently across multiple systems.

## 🔄 Terraform + Ansible

This project fits naturally after Terraform provisioning.

```text
Terraform
    │
    ▼
AWS / EC2
    │
    ▼
Ansible
    │
    ▼
Server Configuration
```

This creates a clean separation:

**Terraform → Infrastructure**

**Ansible → Configuration**

## 🧪 Troubleshooting Workflow

```text
Check inventory
      ↓
Test SSH
      ↓
Run ansible ping
      ↓
Check privileges
      ↓
Check OS / package manager
      ↓
Run with -v
      ↓
Verify system state
```

Common troubleshooting areas:

* SSH keys
* File permissions
* Host addresses
* Python availability
* Sudo permissions
* Package managers
* Service names
* YAML indentation
* Ansible variables

## 📌 Skills Demonstrated

* Ansible fundamentals
* Inventory management
* Playbook execution
* SSH-based automation
* Linux administration
* Configuration management
* Idempotent automation
* Troubleshooting
* Terraform + Ansible workflow

## 🔗 Related DevOps Projects

This repository complements my other projects:

* Terraform AWS Infrastructure
* Cross-OS Ansible Automation
* Kubernetes Projects
* Docker Applications
* AWS EKS
* GitHub Actions
* ArgoCD
* Prometheus
* Grafana

## 👨‍💻 Author

**Sanket Shinde**

GitHub: https://github.com/Sanket4404
