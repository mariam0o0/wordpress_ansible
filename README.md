# WordPress Deployment with Ansible (RedHat-based Systems)

This project automates the deployment of a complete WordPress environment using Ansible on RedHat-based Linux systems (such as CentOS or RHEL). It installs and configures MariaDB, Apache, PHP, and WordPress seamlessly without any manual intervention.

## 📦 Project Structure

```
mywordpress/
├── group_vars/
│   └── all.yaml
├── inventory.ini
├── mywebsite.yaml
├── roles/
│   ├── apache/
│   ├── mariadb/
│   └── wordpress/
└── README.md
```

## ⚙️ Features

- Automated installation of:
  - MariaDB (with secure setup)
  - Apache web server
  - PHP and required extensions
  - WordPress
- OS-aware tasks (RedHat only)
- Uses Ansible roles for modular structure
- Secure MySQL user setup
- Automatically creates the WordPress database and user
- Includes task for installing required Ansible collections

## 🚀 How to Use

### 1. Clone the Repository

```bash
git clone https://github.com/mariam0o0/wordpress_ansible.git
cd wordpress_ansible
```

### 2. Configure Inventory and Variables

- Edit `inventory.ini` to define your target server under `[webservers]`.
- Update `group_vars/all.yaml` with your own database credentials:

### 3. Run the Playbook

```bash
ansible-playbook -i inventory.ini mywebsite.yaml
```

> This will automatically install dependencies, create the database, set up WordPress, and configure Apache.

## 📚 Requirements

- Ansible 2.10+
- Python and pip
- `PyMySQL` installed on the control node
- RedHat-based target system with root or sudo access

## 🧩 Collections Used

This project uses the [`community.mysql`](https://docs.ansible.com/ansible/latest/collections/community/mysql/) Ansible collection.

To install it manually (if needed):

```bash
ansible-galaxy collection install community.mysql
```

## 📄 License

MIT License

---

**Author:**
Aya Abdelatty
Ereny Abdelmesieh
Mariam Yasser 

```

---

Let me know if you want a version with Ubuntu compatibility or want to include screenshots or badges!
