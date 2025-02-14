# Setup VPS

Dokumentasi untuk setup awal VPS Ubuntu dengan Docker, Docker Compose, dan beberapa paket tambahan.

## 1. Update dan Upgrade Sistem
```sh
sudo apt update && sudo apt upgrade -y
```

## 2. Install Paket Pendukung
```sh
sudo apt install -y curl git htop ufw
```

## 3. Install Docker dan Docker Compose
```sh
sudo apt update && sudo apt upgrade -y && sudo apt install -y curl git htop ufw docker-compose && curl -fsSL https://get.docker.com | sh && sudo usermod -aG docker $USER && newgrp docker && sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose && sudo chmod +x /usr/local/bin/docker-compose && docker --version && docker-compose --version
```

## 4. Setup Firewall (Opsional)
```sh
sudo ufw allow OpenSSH
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw enable
```

## 5. Verifikasi Instalasi
Cek apakah Docker dan Docker Compose sudah terpasang dengan benar:
```sh
docker --version && docker-compose --version
```
