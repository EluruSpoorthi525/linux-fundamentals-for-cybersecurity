# Service Management (systemctl)

## Introduction

Linux runs many background programs called **services** (or **daemons**) that perform essential tasks such as remote access, networking, databases, and web hosting. Most modern Linux distributions use **systemd** to manage these services, and the **systemctl** command is used to control them.

Understanding service management is important for Linux administration and cybersecurity because many attacks target vulnerable or unnecessary services.

---

# What is a Service?

A **service** is a background program that starts automatically or manually to perform specific system tasks.

Examples:

- SSH Server (`sshd`)
- Apache (`apache2`)
- Nginx (`nginx`)
- MySQL (`mysql`)
- Docker (`docker`)
- Cron (`cron`)

---

# What is systemd?

**systemd** is the default service manager in most Linux distributions.

It is responsible for:

- Booting the system
- Managing services
- Handling dependencies
- Managing system targets
- Logging events

---

# What is systemctl?

`systemctl` is the command used to manage Linux services.

Common operations include:

- Start services
- Stop services
- Restart services
- Enable services
- Disable services
- Check service status

---

# Common systemctl Commands

Check service status:

```bash
systemctl status ssh
```

Start a service:

```bash
sudo systemctl start nginx
```

Stop a service:

```bash
sudo systemctl stop nginx
```

Restart a service:

```bash
sudo systemctl restart nginx
```

Reload service configuration:

```bash
sudo systemctl reload nginx
```

Enable service at boot:

```bash
sudo systemctl enable nginx
```

Disable service at boot:

```bash
sudo systemctl disable nginx
```

Check if a service is running:

```bash
systemctl is-active nginx
```

List running services:

```bash
systemctl list-units --type=service
```

List failed services:

```bash
systemctl --failed
```

---

# Viewing Service Logs

View logs for a service:

```bash
journalctl -u ssh
```

View the latest logs:

```bash
journalctl -u ssh -n 20
```

Follow logs in real time:

```bash
journalctl -u ssh -f
```

---

# Common Services

| Service | Purpose |
|----------|---------|
| sshd | Remote access |
| nginx | Web server |
| apache2 | Web server |
| mysql | Database |
| docker | Container engine |
| cron | Scheduled tasks |

---

# Best Practices

- Enable only required services.
- Disable unused services.
- Monitor service logs regularly.
- Restart services after configuration changes.
- Avoid stopping critical system services.

---

# Cybersecurity Relevance

Service management helps security professionals to:

- Detect unauthorized services
- Disable unnecessary services
- Monitor critical services
- Investigate service failures
- Reduce the attack surface

---

# Key Takeaways

- Services are background programs.
- `systemd` manages services.
- `systemctl` controls services.
- `journalctl` displays service logs.
- Proper service management improves system security.

---

# Interview Questions

1. What is a Linux service?
2. What is `systemd`?
3. What does `systemctl` do?
4. What is the difference between `start` and `enable`?
5. How do you check a service's status?

---

# Next Topic

➡️ **16-Package-Management.md**
