# 26-Linux-Security-Best-Practices

## Introduction

Linux is considered one of the most secure operating systems, but security depends on proper configuration and maintenance. Following security best practices helps protect systems from unauthorized access, malware, and cyber attacks.

Whether you're a system administrator or a cybersecurity professional, securing Linux should always be a priority.

---

# Why is Linux Security Important?

Linux security helps to:

- Protect sensitive data
- Prevent unauthorized access
- Reduce security risks
- Improve system reliability
- Maintain compliance

---

# Best Practices

### 1. Keep the System Updated

Install the latest security patches regularly.

```bash
sudo apt update
sudo apt upgrade
```

---

### 2. Use Strong Passwords

- Use long and complex passwords.
- Avoid common words.
- Change passwords periodically.

Change password:

```bash
passwd
```

---

### 3. Use the Principle of Least Privilege

Give users only the permissions they need.

Check current user:

```bash
whoami
```

---

### 4. Secure SSH Access

- Disable root login.
- Use SSH key authentication.
- Change the default SSH port (optional).

Check SSH service:

```bash
systemctl status ssh
```

---

### 5. Manage File Permissions

Restrict access to sensitive files.

Example:

```bash
chmod 600 secret.txt
```

---

### 6. Enable a Firewall

Allow only required network traffic.

Ubuntu (UFW):

```bash
sudo ufw enable
```

Check firewall status:

```bash
sudo ufw status
```

---

### 7. Remove Unused Software

Reduce the attack surface by uninstalling unnecessary packages.

```bash
sudo apt autoremove
```

---

### 8. Monitor System Logs

Review logs regularly for suspicious activity.

```bash
journalctl
```

Authentication logs:

```bash
cat /var/log/auth.log
```

---

### 9. Backup Important Data

Create regular backups to prevent data loss.

Example:

```bash
tar -czvf backup.tar.gz /home/user
```

---

### 10. Disable Unnecessary Services

List running services:

```bash
systemctl list-units --type=service
```

Disable an unused service:

```bash
sudo systemctl disable apache2
```

---

# Security Checklist

- ✔ Keep the system updated
- ✔ Use strong passwords
- ✔ Enable a firewall
- ✔ Secure SSH access
- ✔ Monitor system logs
- ✔ Backup important data
- ✔ Remove unused software
- ✔ Disable unnecessary services

---

# Cybersecurity Relevance

Linux security best practices help:

- Prevent unauthorized access
- Reduce attack surfaces
- Detect suspicious activities
- Protect sensitive information
- Improve incident response

These practices form the foundation of a secure Linux environment.

---

# Key Takeaways

- Keep Linux updated.
- Use strong authentication methods.
- Follow the Principle of Least Privilege.
- Secure SSH and file permissions.
- Monitor logs and backup data regularly.

---

# Interview Questions

1. Why is it important to keep Linux updated?
2. What is the Principle of Least Privilege?
3. How does a firewall improve security?
4. Why should unnecessary services be disabled?
5. Why are backups important?

---

# Next Topic

➡️ **27-Linux-for-Cybersecurity.md**
