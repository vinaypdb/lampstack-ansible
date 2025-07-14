# 🔧 LAMP Stack Automation with Ansible

This project automates the installation and configuration of a **LAMP stack** (Linux, Apache, MySQL, PHP) on Ubuntu using **Ansible**.

---

## 📌 Features

- ✅ Installs and enables Apache
- ✅ Installs MySQL Server
- ✅ Installs PHP and integrates it with Apache
- ✅ Sets up a custom Apache Virtual Host (`mysite.local`)
- ✅ Adds a sample `index.php` file
- ✅ Configures UFW (firewall) to allow Apache traffic
- ✅ Uses modular and idempotent Ansible roles

---

## 📁 Folder Structure
```

lampstack-ansible/
├── inventory
├── playbook.yml
├── README.md
├── .gitignore
└── roles/
├── apache/
│ └── tasks/main.yml
├── mysql/
│ └── tasks/main.yml
├── php/
│ └── tasks/main.yml
├── ufw/
│ └── tasks/main.yml
└── virtualhost/
├── tasks/main.yml
├── handlers/main.yml
└── templates/vhost.conf.j2
```


---

## 🚀 Getting Started

### 🛠️ Prerequisites

- Ubuntu system (local or remote)
- Python & Ansible installed
- SSH access (if deploying remotely)

### 📥 Clone the Repository

```bash
git clone https://github.com/<your-username>/lampstack-ansible.git
cd lampstack-ansible








































