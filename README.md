# Ansible Role: QEMU Guest Agent 🚀
![GitHub release (with filter)](https://img.shields.io/github/v/release/philippwaller/ansible-role-qemu_guest_agent)
![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/philippwaller/ansible-role-qemu_guest_agent/ci.yaml)
![Ansible Role](https://img.shields.io/ansible/role/d/philippwaller/qemu_guest_agent)
![GitHub Repo stars](https://img.shields.io/github/stars/philippwaller/ansible-role-qemu_guest_agent)
![GitHub License](https://img.shields.io/github/license/philippwaller/ansible-role-qemu_guest_agent)

> Enhance your virtualization experience with the power of QEMU Guest Agent! 🌐✨

This role simplifies the process of installing and configuring the QEMU Guest Agent on VMs running under QEMU/KVM 
virtualization, offering improved performance and advanced management features.

## 🌟 Key Features
- 🛠 **Effortless Setup:** Streamlines the installation of QEMU Guest Agent.
- 🚀 **Service Activation:** Ensures the QEMU Guest Agent service is up and running.

## 🚀 Getting Started

### 📋 Prerequisites
- **Ansible Installed:** Ensure Ansible is installed on your management machine. [Ansible Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/index.html)
- **Python on Target System:** The target system must have Python installed for Ansible modules to function correctly.
For systems lacking Python, consider using [Robert de Bock's Bootstrap Role](https://galaxy.ansible.com/robertdebock/bootstrap) 
to prepare your hosts.

### 📥 Installation
Install the role via Ansible Galaxy:

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
| Variable                                | Default | Description                                                                                                                                                                                                |
|-----------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `qemu_guest_agent_update_package_cache` | `false` | This variable controls whether the package cache should be updated before installing the QEMU Guest Agent. Setting it to false can speed up the role execution if the package cache is already up-to-date. |


## 🤝 Contributing
🌟 Contributions make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

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