# 24-Log-Analysis

## Introduction

Log analysis is the process of examining log files to monitor system activity, troubleshoot issues, detect security incidents, and identify suspicious behavior. Linux stores logs that record system events, user logins, application activities, and errors.

For cybersecurity professionals, log analysis is one of the most important skills for threat detection and incident response.

---

# What are Log Files?

Log files are text files that record events occurring on a Linux system.

They help administrators to:

- Monitor system health
- Troubleshoot problems
- Detect unauthorized access
- Investigate security incidents
- Audit user activities

---

# Common Log Locations

| Log File | Purpose |
|----------|---------|
| `/var/log/syslog` | General system logs |
| `/var/log/auth.log` | Authentication and login logs |
| `/var/log/kern.log` | Kernel logs |
| `/var/log/dmesg` | Boot and hardware logs |
| `/var/log/boot.log` | Boot process logs |

> **Note:** On Red Hat-based systems, authentication logs are usually stored in `/var/log/secure`.

---

# Viewing Log Files

Display an entire log file:

```bash
cat /var/log/syslog
```

View logs page by page:

```bash
less /var/log/syslog
```

View the last 10 lines:

```bash
tail /var/log/syslog
```

Follow logs in real time:

```bash
tail -f /var/log/syslog
```

View the first 10 lines:

```bash
head /var/log/syslog
```

---

# Searching Logs

Search for a keyword:

```bash
grep "Failed" /var/log/auth.log
```

Search for SSH activity:

```bash
grep "ssh" /var/log/auth.log
```

---

# Using journalctl

Modern Linux systems use **systemd**, which stores logs in the system journal.

View all logs:

```bash
journalctl
```

View recent logs:

```bash
journalctl -n 20
```

View logs for the SSH service:

```bash
journalctl -u ssh
```

---

# Why Log Analysis Matters

Log analysis helps you:

- Detect failed login attempts
- Identify suspicious activities
- Troubleshoot system errors
- Monitor services
- Support incident investigations

---

# Best Practices

- Review logs regularly.
- Archive important logs.
- Protect log files from unauthorized access.
- Monitor failed login attempts.
- Rotate logs to save disk space.

---

# Cybersecurity Relevance

Security analysts use log analysis to:

- Detect brute-force attacks
- Investigate compromised systems
- Monitor authentication events
- Identify malware activity
- Collect forensic evidence

Example:

```bash
grep "Failed password" /var/log/auth.log
```

This command displays failed SSH login attempts, which may indicate a brute-force attack.

---

# Key Takeaways

- Log files record system and application events.
- Linux stores logs in `/var/log/`.
- `cat`, `less`, `head`, and `tail` help view logs.
- `grep` searches log files.
- `journalctl` displays systemd logs.
- Log analysis is essential for troubleshooting and cybersecurity.

---

# Interview Questions

1. What is log analysis?
2. Where are Linux log files stored?
3. What does the `tail -f` command do?
4. What is the purpose of `journalctl`?
5. How can log analysis help detect cyber attacks?

---

# Next Topic

➡️ **25-Scheduling-Tasks-with-Cron.md**
