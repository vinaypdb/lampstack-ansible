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
    │   └── tasks/
    │       └── main.yml
    ├── mysql/
    │   └── tasks/
    │       └── main.yml
    ├── php/
    │   └── tasks/
    │       └── main.yml
    ├── ufw/
    │   └── tasks/
    │       └── main.yml
    └── virtualhost/
        ├── tasks/
        │   └── main.yml
        ├── handlers/
        │   └── main.yml
        └── templates/
            └── vhost.conf.j2
```

---

## 🚀 Getting Started

### 🛠️ Prerequisites

- Ubuntu system (local or remote)
- Python & Ansible installed
- SSH access (if deploying remotely)

---

### 📥 Clone the Repository

```bash
git clone https://github.com/<your-username>/lampstack-ansible.git
cd lampstack-ansible
```

---

### ⚙️ Configure Inventory

#### For local machine:

```ini
# inventory
[lamp]
localhost ansible_connection=local
```

#### For remote server:

```ini
# inventory
[lamp]
your_server_ip ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/id_rsa
```

---

## ▶️ Run the Playbook

```bash
ansible-playbook -i inventory playbook.yml
```

---

## 🌐 Access Your Website

### 🧪 For local machine testing:

Edit your `/etc/hosts` file:

```bash
sudo nano /etc/hosts
```

Add:

```
127.0.0.1 mysite.local
```

Then visit: [http://mysite.local](http://mysite.local)

---

## 🧾 Output

- Apache runs with a PHP homepage
- MySQL service is installed and active
- Firewall allows HTTP (Apache)
- `mysite.local` points to a real working virtual host with `phpinfo()` test page

---

## 🚧 TODO (Optional Enhancements)

- 🔐 Secure MySQL root password using Ansible
- 🛡️ Add SSL using Let's Encrypt and Certbot
- 🧪 Add idempotency checks or Molecule testing
- 📦 Refactor roles into reusable Galaxy collections
- 🧼 Add CI/CD with `ansible-lint` and GitHub Actions

---

## 📦 .gitignore

```
*.retry
*.log
*.swp
*.bak
__pycache__/
.cache/
.ansible/
```

---

## 👨‍💻 Author

**Your Name**  
GitHub: [@yourgithub](https://github.com/yourgithub)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.