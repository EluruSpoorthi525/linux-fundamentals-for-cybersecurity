# 25-Scheduling-Tasks-with-Cron

## Introduction

**Cron** is a built-in Linux utility used to schedule commands or scripts to run automatically at specified times or intervals. It is commonly used for automating system maintenance, backups, updates, log rotation, and other repetitive tasks.

Cron helps system administrators save time by eliminating the need to manually execute recurring tasks.

---

# What is Cron?

Cron is a **job scheduler** that runs tasks automatically based on a schedule defined by the user.

Each scheduled task is called a **Cron Job**.

---

# What is Crontab?

A **Crontab (Cron Table)** is a file that stores scheduled cron jobs for a user.

Edit your crontab:

```bash
crontab -e
```

View existing cron jobs:

```bash
crontab -l
```

Remove all cron jobs:

```bash
crontab -r
```

---

# Cron Job Syntax

```text
* * * * * command
│ │ │ │ │
│ │ │ │ └── Day of the Week (0–7)
│ │ │ └──── Month (1–12)
│ │ └────── Day of Month (1–31)
│ └──────── Hour (0–23)
└────────── Minute (0–59)
```

---

# Common Cron Examples

Run a script every day at 2:00 AM:

```bash
0 2 * * * /home/user/backup.sh
```

Run every hour:

```bash
0 * * * * command
```

Run every 30 minutes:

```bash
*/30 * * * * command
```

Run every Sunday at 6:00 PM:

```bash
0 18 * * 0 command
```

Run every reboot:

```bash
@reboot /home/user/startup.sh
```

---

# Special Cron Keywords

| Keyword | Description |
|----------|-------------|
| `@reboot` | Run at system startup |
| `@hourly` | Every hour |
| `@daily` | Once every day |
| `@weekly` | Once every week |
| `@monthly` | Once every month |
| `@yearly` | Once every year |

---

# Managing the Cron Service

Check cron service status:

```bash
systemctl status cron
```

On Red Hat-based systems:

```bash
systemctl status crond
```

Start the cron service:

```bash
sudo systemctl start cron
```

Enable cron at boot:

```bash
sudo systemctl enable cron
```

---

# Best Practices

- Test scripts before scheduling them.
- Use absolute file paths.
- Review cron jobs regularly.
- Keep scheduled tasks documented.
- Remove unused cron jobs.

---

# Cybersecurity Relevance

Cron is widely used in cybersecurity to:

- Schedule automatic backups
- Run security scans
- Rotate log files
- Monitor system health
- Automate maintenance tasks

Attackers may also misuse cron jobs to maintain persistence on compromised systems. Regularly reviewing cron jobs helps detect unauthorized scheduled tasks.

---

# Key Takeaways

- Cron automates repetitive tasks.
- A scheduled task is called a cron job.
- `crontab -e` edits cron jobs.
- `crontab -l` lists scheduled jobs.
- `@reboot` runs a task at system startup.
- Cron is useful for automation and system maintenance.

---

# Interview Questions

1. What is Cron?
2. What is a Crontab?
3. Which command edits cron jobs?
4. What does `@reboot` do?
5. Why is Cron important in Linux administration?

---

# Next Topic

➡️ **26-Linux-Security-Best-Practices.md**
