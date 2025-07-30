# DevOps Portfolio

This repository documents my hands-on learning journey through a 3-week intensive DevOps program. Each folder represents tools, practices, or infrastructure-as-code components I’ve used, while this README tracks my daily progress.


## 📅 Day 1 — Foundations of DevOps


### ✅ Goals Achieved:
- Understood core **DevOps concepts** and responsibilities.
- Learned about **DevOps culture and practices** (Agile, collaboration, CI/CD pipelines, shift-left testing).
- Explored **Kubernetes & orchestration** (high-level overview).
- Reviewed **Git** and popular **Git workflows** (feature branching, pull requests, rebasing, etc).
- Set up a structured DevOps portfolio:
```

devops-portfolio/
├── README.md
├── docker/
│   └── flask-guestbook/
├── ci-cd/
│   └── github-actions/
├── monitoring/
│   └── netdata/
├── infra-as-code/
│   └── terraform-digitalocean/
├── notes/
│   ├── git.md
│   ├── kubernetes.md
│   └── devops-glossary.md

````
- Initialized the repo with Git, renamed `master` to `main`, resolved branch conflicts, pulled from remote, and pushed successfully.


## 📅 Day 2 — EC2 Deep Dive + Server Setup


### ✅ Goals Achieved:
- Launched an **EC2 instance** on AWS using Ubuntu Server.
- Configured:
- **Security Groups** (port 22 for SSH, 80 for HTTP).
- **EBS volume** and verified disk space.
- Used **SSH** to access the EC2 instance securely via:
```bash
ssh -i devop-key.pem ubuntu@16.171.165.232
````

* Learned why **root login is disabled by default** in AWS (security best practice).
* Performed **system updates**:

  ```bash
  sudo apt update && sudo apt upgrade -y
  ```
* Installed and configured:

  * **NGINX** as a basic web server.
  * A basic HTML page via `vim` editor in `/var/www/html/index.nginx-debian.html`.
* Used `vim` to **create and edit** files directly on the EC2 server.
* Enabled **UFW firewall** and allowed OpenSSH + NGINX:

  ```bash
  sudo ufw allow OpenSSH
  sudo ufw allow 'Nginx HTTP'
  sudo ufw enable
  ```

### 🔧 Tools Used:

* AWS EC2
* NGINX
* UFW
* SSH
* vim editor

