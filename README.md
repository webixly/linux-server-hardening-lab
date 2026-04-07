# 🔐 Linux Server Hardening Lab

## 📌 Overview

This project demonstrates how to secure a Linux server by implementing essential security measures:

* SSH key-based authentication (no password login)
* UFW firewall configuration
* Fail2Ban protection against brute-force attacks

---

## ⚙️ Technologies Used

* Ubuntu Server 24.04
* OpenSSH
* UFW (Uncomplicated Firewall)
* Fail2Ban

---

## 🔐 SSH Key Authentication

Password login was replaced with SSH key authentication for improved security.

![SSH Login](screenshots/ssh-login.png)

---

## 🔥 UFW Firewall Configuration

Firewall is configured to deny all incoming traffic except SSH (port 22).

![UFW Status](screenshots/ufw.png)

---

## 🚫 Fail2Ban Protection

Fail2Ban detects and blocks brute-force attacks on SSH.

![Fail2Ban](screenshots/fail2ban.png)

---

## 🛡️ Security Improvements

* Disabled password authentication (SSH)
* Enabled firewall rules
* Protected against brute-force attacks
* Reduced attack surface

---

## 📈 Result

The server is now significantly more secure against common attacks such as:

* Unauthorized SSH access
* Brute-force login attempts
* Open port exploitation

---

## 👨‍💻 Author

* GitHub: https://github.com/webixly
