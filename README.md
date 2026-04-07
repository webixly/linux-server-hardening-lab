# 🔐 Linux Server Hardening Lab
![Linux](https://img.shields.io/badge/Linux-Ubuntu-orange)
![Security](https://img.shields.io/badge/Security-Hardening-blue)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

This project demonstrates how to secure a Linux server (Ubuntu 24.04) using practical system administration techniques.

The objective is to reduce the attack surface and protect the server against unauthorized access and brute-force attacks.

---

## 🚀 Quick Summary

A practical Linux server hardening project demonstrating:

- 🔐 Secure SSH access using key authentication (no passwords)
- 🔥 Firewall protection using UFW
- 🚫 Automatic brute-force protection with Fail2Ban

This lab simulates real-world system administration tasks and security practices.

## 📌 Overview

This lab includes:

* SSH key-based authentication (password login disabled)
* UFW firewall configuration
* Fail2Ban protection against brute-force attacks

---

## ⚠️ Security Threats

Before hardening, the server was vulnerable to:

* Brute-force SSH attacks
* Unauthorized access via password login
* Exploitation of open ports

---

## 🛡️ Mitigation Strategy

The following measures were implemented:

* Disabled password authentication → prevents brute-force attacks
* Configured UFW firewall → restricts incoming connections
* Enabled Fail2Ban → automatically blocks suspicious IPs

---

## 🚀 Technologies Used

* Ubuntu Server 24.04
* OpenSSH
* UFW (Uncomplicated Firewall)
* Fail2Ban

---

## ⚙️ Implementation

### 🔑 SSH Key Authentication

Password-based login was replaced with SSH key authentication.

* Generated an ed25519 key pair
* Connected from a Windows client
* Disabled password authentication in SSH configuration

---

### 🔥 UFW Firewall Configuration

* Deny all incoming connections
* Allow outgoing connections
* Allow SSH (port 22)

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 22
sudo ufw enable
```

---

### 🚫 Fail2Ban Protection

* Installed and configured Fail2Ban
* Enabled SSH protection
* Automatically blocks suspicious IP addresses

```bash
sudo apt install fail2ban -y
sudo systemctl enable fail2ban
sudo systemctl start fail2ban
```

---

## 🔍 Before vs After

| Aspect      | Before ❌ | After ✅            |
| ----------- | -------- | ------------------ |
| SSH Login   | Password | SSH Key only       |
| Firewall    | Disabled | Enabled (UFW)      |
| Brute-force | Possible | Blocked (Fail2Ban) |

---

## 🔒 Security Improvements

* Password authentication disabled
* Firewall rules enforced
* Brute-force attacks mitigated
* Reduced attack surface

---

## 📸 Screenshots

### SSH Key Authentication

![SSH Login](screenshots/ssh-login.png)

### Fail2Ban Protection

![Fail2Ban](screenshots/fail2ban.png)

### UFW Firewall Status

![UFW](screenshots/ufw.png)

---

## 📌 Conclusion

This project shows how basic hardening techniques can significantly improve the security of a Linux server.

It serves as a practical example for aspiring system administrators and IT professionals.
🇩🇪 German version: [README-DE.md](README-DE.md)
---

## 👤 Author

* Pablo (Webixly)
* GitHub: https://github.com/webixly
