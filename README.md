# 🔐 Linux Server Hardening Lab

This project demonstrates how to secure a Linux server using real-world system administration practices.
It focuses on SSH hardening, firewall configuration, and protection against brute-force attacks.

---

## 🚀 Overview

In this lab, I configured and secured an Ubuntu server by applying multiple layers of security:

* SSH key-based authentication (password login disabled)
* UFW firewall configuration
* Fail2Ban intrusion prevention system
* Real brute-force attack simulation and mitigation

---

## 🛠️ Technologies Used

* Ubuntu Server 24.04 LTS
* OpenSSH
* UFW (Uncomplicated Firewall)
* Fail2Ban

---

## 🔐 SSH Hardening

* Generated SSH key pair (ed25519)
* Disabled password authentication
* Secured remote access using key-based login only

```bash
sudo nano /etc/ssh/sshd_config
```

```text
PasswordAuthentication no
PermitRootLogin no
PubkeyAuthentication yes
```

---

## 🔥 Firewall Configuration (UFW)

* Default deny incoming traffic
* Allow SSH (port 22)

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 22
sudo ufw enable
```

---

## 🛡️ Fail2Ban Protection

* Installed and configured Fail2Ban for SSH
* Automatic banning of IP after failed login attempts

```bash
sudo apt install fail2ban -y
```

```ini
[sshd]
enabled = true
maxretry = 3
bantime = 3600
findtime = 600
```

---

## 💣 Attack Simulation

Simulated brute-force attack by attempting multiple failed SSH logins.

Result:

* IP address automatically banned by Fail2Ban
* Connection blocked (timeout)

```bash
sudo fail2ban-client status sshd
```

Example output:

```
Currently banned: 1
Banned IP list: 192.168.xxx.xxx
```

---

## 📸 Proof

(Add your screenshots here)

* SSH login without password
* Fail2Ban banning IP
* UFW status

---

## 🧠 What I Learned

* How SSH authentication works internally
* Importance of disabling password-based access
* How to secure a Linux server against brute-force attacks
* Monitoring and testing security mechanisms

---

## ⚡ Future Improvements

* VPN (WireGuard)
* Log monitoring and alerting
* Automation scripts (Bash)

---

## 📌 Author

Aymen (Webixly)
