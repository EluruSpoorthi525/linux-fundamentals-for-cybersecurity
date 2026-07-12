# 21-SSH-and-Remote-Access

## Introduction

**SSH (Secure Shell)** is a secure network protocol used to remotely access and manage Linux systems over a network. It encrypts all communication between the client and the server, making remote administration safe from eavesdropping and attacks.

SSH is one of the most important tools for Linux administrators, cloud engineers, DevOps professionals, and cybersecurity experts.

---

# Why Use SSH?

SSH helps you to:

- Access remote Linux systems securely
- Transfer files safely
- Execute remote commands
- Manage servers from anywhere
- Encrypt network communication

---

# SSH Components

- **SSH Client** – The system initiating the connection.
- **SSH Server** – The remote system accepting the connection.

---

# Basic SSH Command

Connect to a remote server:

```bash
ssh username@hostname
```

Example:

```bash
ssh user@192.168.1.10
```

---

# SSH Using a Custom Port

If the SSH server uses a different port:

```bash
ssh -p 2222 user@192.168.1.10
```

---

# Generate SSH Key Pair

Create a public and private key:

```bash
ssh-keygen
```

Default location:

```text
~/.ssh/
```

Files created:

- `id_rsa` → Private Key
- `id_rsa.pub` → Public Key

---

# Copy Public Key to Server

```bash
ssh-copy-id user@192.168.1.10
```

This enables passwordless login.

---

# Secure File Transfer

Copy a file to a remote server:

```bash
scp file.txt user@192.168.1.10:/home/user/
```

Copy a file from a remote server:

```bash
scp user@192.168.1.10:/home/user/file.txt .
```

---

# SFTP (Secure File Transfer Protocol)

Connect using SFTP:

```bash
sftp user@192.168.1.10
```

Useful commands:

```bash
ls
pwd
get file.txt
put file.txt
exit
```

---

# Check SSH Service Status

```bash
systemctl status ssh
```

or

```bash
systemctl status sshd
```

*(Depends on the Linux distribution.)*

---

# Start SSH Service

```bash
sudo systemctl start ssh
```

---

# Enable SSH at Boot

```bash
sudo systemctl enable ssh
```

---

# Best Practices

- Use SSH key authentication instead of passwords.
- Disable root login over SSH.
- Use strong passwords or passphrases.
- Keep the SSH server updated.
- Restrict SSH access using a firewall.

---

# Cybersecurity Relevance

SSH is widely used for:

- Secure remote administration
- Incident response
- Server management
- Secure file transfers
- Accessing cloud servers
- Managing security tools remotely

Misconfigured SSH services can become a target for brute-force attacks, making proper configuration essential.

---

# Key Takeaways

- SSH provides encrypted remote access.
- `ssh` connects to remote systems.
- `ssh-keygen` creates authentication keys.
- `scp` securely transfers files.
- `sftp` enables secure file management.
- SSH key authentication is more secure than passwords.

---

# Interview Questions

1. What is SSH?
2. What is the default SSH port?
3. What is the difference between SSH and Telnet?
4. What does `ssh-keygen` do?
5. What is the purpose of `scp`?

---

# Next Topic

➡️ **23-Linux-Security-Basics.md**
