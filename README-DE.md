# 🔐 Linux Server Hardening Lab

## 📌 Übersicht

Dieses Projekt zeigt, wie man einen Linux-Server sicherer macht, indem man wichtige Sicherheitsmaßnahmen umsetzt.

Das Ziel ist es, den Server vor häufigen Angriffen wie Brute-Force-Attacken zu schützen.

---

## ⚙️ Verwendete Technologien

* Ubuntu Server 24.04
* OpenSSH
* UFW (Firewall)
* Fail2Ban

---

## 🔐 SSH-Key-Authentifizierung

Die Anmeldung mit Passwort wurde deaktiviert.
Stattdessen wird eine sichere SSH-Key-Authentifizierung verwendet.

![SSH Login](screenshots/ssh-login.png)

---

## 🔥 Firewall (UFW)

Die Firewall wurde so konfiguriert, dass alle eingehenden Verbindungen blockiert werden, außer SSH (Port 22).

![UFW Status](screenshots/ufw.png)

---

## 🚫 Fail2Ban Schutz

Fail2Ban erkennt fehlgeschlagene Login-Versuche und sperrt automatisch verdächtige IP-Adressen.

![Fail2Ban](screenshots/fail2ban.png)

---

## 🛡️ Sicherheitsmaßnahmen

* Deaktivierung der Passwort-Authentifizierung
* Verwendung von SSH-Schlüsseln
* Aktivierung der Firewall (UFW)
* Schutz gegen Brute-Force-Angriffe mit Fail2Ban

---

## 📈 Ergebnis

Der Server ist jetzt besser geschützt gegen:

* Unbefugten Zugriff
* Brute-Force-Angriffe
* Unsichere Verbindungen

---

## 👨‍💻 Autor

GitHub: https://github.com/webixly
