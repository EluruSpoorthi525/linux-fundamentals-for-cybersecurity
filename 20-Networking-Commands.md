# 20-Networking-Commands

## Introduction

Linux provides powerful networking commands that help users configure, troubleshoot, and monitor network connections. These commands are essential for Linux administrators, network engineers, and cybersecurity professionals to diagnose connectivity issues and analyze network traffic.

---

# Why Learn Networking Commands?

Networking commands help you:

- Check network connectivity
- View IP addresses
- Troubleshoot network issues
- Test DNS resolution
- Monitor open ports
- Transfer files
- Download files from the internet

---

# ip

The `ip` command is used to view and configure network interfaces.

Display IP address:

```bash
ip addr
```

Display routing table:

```bash
ip route
```

Show network interfaces:

```bash
ip link
```

---

# ping

Tests connectivity between your computer and another host.

Syntax:

```bash
ping google.com
```

Example:

```bash
ping 8.8.8.8
```

Stop with **Ctrl + C**.

---

# hostname

Displays or sets the system hostname.

View hostname:

```bash
hostname
```

View IP address:

```bash
hostname -I
```

---

# ifconfig

Displays network interface information.

```bash
ifconfig
```

> **Note:** `ifconfig` is deprecated on most modern Linux distributions. Use `ip addr` instead.

---

# ss

Displays network sockets and active connections.

Show listening ports:

```bash
ss -tuln
```

---

# netstat

Displays network connections, routing tables, and listening ports.

```bash
netstat -tuln
```

> **Note:** `ss` is the modern replacement for `netstat`.

---

# traceroute

Shows the path packets take to reach a destination.

```bash
traceroute google.com
```

---

# nslookup

Queries DNS servers for domain information.

```bash
nslookup google.com
```

---

# dig

Provides detailed DNS information.

```bash
dig google.com
```

---

# curl

Transfers data from or to a server.

Download a webpage:

```bash
curl https://example.com
```

View HTTP headers:

```bash
curl -I https://example.com
```

---

# wget

Downloads files from the internet.

Download a file:

```bash
wget https://example.com/file.zip
```

---

# scp

Securely copies files between systems over SSH.

Copy file to remote system:

```bash
scp file.txt user@server:/home/user/
```

Copy file from remote system:

```bash
scp user@server:/home/user/file.txt .
```

---

# Common Networking Commands

| Command | Purpose |
|----------|---------|
| `ip` | View and configure network interfaces |
| `ping` | Test network connectivity |
| `hostname` | Display system hostname |
| `ss` | Show network connections |
| `netstat` | Display network statistics |
| `traceroute` | Trace packet path |
| `nslookup` | DNS lookup |
| `dig` | Detailed DNS information |
| `curl` | Transfer data from servers |
| `wget` | Download files |
| `scp` | Secure file transfer |

---

# Best Practices

- Use `ip` instead of `ifconfig`.
- Verify connectivity using `ping`.
- Check open ports regularly.
- Use `scp` instead of insecure file transfer methods.
- Monitor network connections for suspicious activity.

---

# Cybersecurity Relevance

Networking commands are essential for:

- Troubleshooting connectivity issues
- Checking open ports
- Verifying DNS records
- Downloading security tools
- Secure file transfers
- Investigating network incidents

---

# Key Takeaways

- `ip` manages network interfaces.
- `ping` tests connectivity.
- `ss` displays active network connections.
- `nslookup` and `dig` perform DNS lookups.
- `curl` and `wget` retrieve data from the internet.
- `scp` securely transfers files over SSH.

---

# Interview Questions

1. What is the difference between `ip` and `ifconfig`?
2. What does the `ping` command do?
3. Which command displays active network connections?
4. What is the purpose of `nslookup`?
5. What is the difference between `curl` and `wget`?

---

# Next Topic

➡️ **21-Shell-Scripting-Basics.md**
