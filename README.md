# 🔐 Linux Server Hardening Lab

This project demonstrates how to secure a Linux server (Ubuntu 24.04) by implementing essential security measures.

The goal is to reduce attack surface and protect the server from unauthorized access and brute-force attacks.

---

## 📌 Overview

This lab includes:

* SSH key-based authentication (no password login)
* UFW firewall configuration
* Fail2Ban protection against brute-force attacks

---

## ⚠️ Security Threats

Before hardening, the server was vulnerable to:

* Brute-force SSH attacks
* Unauthorized access via password login
* Open port exploitation

---

## 🛡️ Mitigation Strategy

To secure the system, the following actions were taken:

* Disabled password authentication → prevents brute-force attacks
* Configured UFW firewall → restricts incoming traffic
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

Password login was replaced with SSH key authentication.

* Generated ed25519 key
* Connected from client (Windows)
* Disabled password authentication in SSH config

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

See the `/screenshots` folder for:

* SSH login
* UFW status
* Fail2Ban status

---

## 📌 Conclusion

This project shows how basic hardening techniques can significantly improve the security of a Linux server.

It is a practical example for aspiring system administrators and IT professionals.

---

## 👤 Author

* Pablo (Webixly)
* GitHub: [https://github.com/webixly](https://github.com/webixly)
