# Ansible Role: QEMU Guest Agent 🚀
[![GitHub release (with filter)](https://img.shields.io/github/v/release/philippwaller/ansible-role-qemu_guest_agent)](https://github.com/philippwaller/ansible-role-qemu_guest_agent/releases)
[![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/philippwaller/ansible-role-qemu_guest_agent/ci.yaml)](https://github.com/philippwaller/ansible-role-qemu_guest_agent/actions/workflows/ci.yaml)
[![Ansible Role](https://img.shields.io/ansible/role/d/philippwaller/qemu_guest_agent)](https://galaxy.ansible.com/ui/standalone/roles/philippwaller/qemu_guest_agent/)
[![GitHub Repo stars](https://img.shields.io/github/stars/philippwaller/ansible-role-qemu_guest_agent)](https://github.com/philippwaller/ansible-role-qemu_guest_agent)
[![GitHub License](https://img.shields.io/github/license/philippwaller/ansible-role-qemu_guest_agent)](https://github.com/philippwaller/ansible-role-qemu_guest_agent/blob/main/LICENSE.md)

> Enhance your virtualization experience with the power of QEMU Guest Agent! 🌐✨

This role simplifies the process of installing and configuring the QEMU Guest Agent on VMs running under QEMU/KVM      
virtualization, offering improved performance and advanced management features.

## 🌟 Key Features

- 🛠 **Effortless Setup:** Streamlines the installation of QEMU Guest Agent.
- 🚀 **Service Activation:** Ensures the QEMU Guest Agent service is up and running.

## 🚀 Getting Started

### 📋 Prerequisites

To successfully use this Ansible role, please ensure that your systems meet the following requirements:

- **Ansible:** Your management system must have ansible-core 2.15 (equivalent to Ansible 8.0.0) or higher installed. For
detailed installation instructions, refer to the [Ansible Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/index.html).
- **Python on Target System:** Python is required on the target system for the correct functioning of Ansible modules. 
For systems lacking Python, consider using [Robert de Bock's Bootstrap Role](https://galaxy.ansible.com/robertdebock/bootstrap)
to prepare your hosts.

### 📥 Installation

Install the role via [Ansible Galaxy](https://galaxy.ansible.com/ui/standalone/roles/philippwaller/qemu_guest_agent/):

```shell
ansible-galaxy install philippwaller.qemu_guest_agent
```

### 📘 Example Playbook

Easily integrate this role into your playbook:

```yaml
---
- name: Install QEMU Guest Agent
  hosts: all

  roles:
    - role: philippwaller.qemu_guest_agent
      qemu_guest_agent_update_package_cache: true
```

### 🎛 Usage

Deploy to your hosts with:

```shell
ansible-playbook your-playbook.yml
```

### ⚙️ Role Variables

The default values for the variables are set in [`defaults/main.yaml`](defaults/main.yaml):

```yaml
---
# Controls whether the package cache should be updated before installing the QEMU Guest Agent.
qemu_guest_agent_update_package_cache: false
```

## 🌍 Supported Operating Systems

This role is compatible with the following operating systems:

- CentOS: 7, 8
- Debian: 10 (Buster), 11 (Bullseye), 12 (Bookworm)
- Fedora: 34, 35, 36, 37, 38, 39
- Rocky Linux: 8, 9
- Ubuntu: 18.04 (Bionic Beaver), 20.04 (Focal Fossa), 22.04 (Jammy Jellyfish)

## 🤝 Contributing

Contributions make the open-source community an amazing place to learn, inspire, and create. Any contributions you make 
are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### 🛠 Pre-Commit Hooks

We use [pre-commit](https://pre-commit.com/) for code quality:

```shell
pip install pre-commit
pre-commit install
pre-commit run
```

## ⭐️ Show Your Support

Love this project? Please consider giving it a ⭐️ on [GitHub](https://github.com/philippwaller/ansible-role-qemu_guest_agent)!

## 📜 License

This project is licensed under the MIT License - see the [`LICENSE.md`](https://github.com/philippwaller/ansible-role-qemu_guest_agent/blob/master/LICENSE.md) file for details.
