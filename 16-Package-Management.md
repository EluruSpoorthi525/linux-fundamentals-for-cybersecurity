# Package Management

## Introduction

Linux uses **package managers** to install, update, remove, and manage software efficiently. Instead of downloading applications manually, package managers retrieve software from trusted repositories while automatically handling dependencies.

Package management is an essential Linux administration skill and plays a crucial role in keeping systems secure and up to date.

---

# What is a Package?

A **package** is a compressed file containing:

- Application files
- Configuration files
- Documentation
- Dependencies
- Installation information

Examples:

- `.deb` (Debian/Ubuntu)
- `.rpm` (Red Hat/Fedora)
- `.pkg.tar.zst` (Arch Linux)

---

# What is a Package Manager?

A **package manager** is a tool used to install, update, upgrade, and remove software.

Benefits:

- Easy software installation
- Automatic dependency management
- Security updates
- Software removal
- Version management

---

# Popular Package Managers

| Distribution | Package Manager |
|--------------|-----------------|
| Ubuntu/Debian | APT |
| Fedora | DNF |
| RHEL/CentOS | YUM / DNF |
| Arch Linux | Pacman |
| openSUSE | Zypper |

---

# Common APT Commands

Update package list:

```bash
sudo apt update
```

Upgrade installed packages:

```bash
sudo apt upgrade
```

Install a package:

```bash
sudo apt install git
```

Remove a package:

```bash
sudo apt remove git
```

Remove package with configuration files:

```bash
sudo apt purge git
```

Remove unused dependencies:

```bash
sudo apt autoremove
```

Search for a package:

```bash
apt search nginx
```

Display package information:

```bash
apt show nginx
```

List installed packages:

```bash
apt list --installed
```

---

# Other Package Managers

### DNF (Fedora)

```bash
sudo dnf install nginx
sudo dnf update
sudo dnf remove nginx
```

### YUM (Older CentOS)

```bash
sudo yum install nginx
sudo yum update
sudo yum remove nginx
```

### Pacman (Arch Linux)

```bash
sudo pacman -S nginx
sudo pacman -Syu
sudo pacman -R nginx
```

---

# Repositories

A **repository** is an online storage location that contains software packages.

Benefits:

- Trusted software
- Automatic updates
- Verified packages
- Easy installation

---

# Best Practices

- Install software from trusted repositories.
- Keep packages updated.
- Remove unused software.
- Regularly install security updates.
- Avoid downloading software from unknown sources.

---

# Cybersecurity Relevance

Package management helps security professionals to:

- Install security tools
- Apply security patches
- Remove vulnerable software
- Keep systems up to date
- Reduce security risks

Examples of security tools:

```bash
sudo apt install nmap
sudo apt install wireshark
sudo apt install tcpdump
```

---

# Key Takeaways

- Packages contain software and related files.
- Package managers automate software management.
- APT is used on Ubuntu/Debian.
- DNF is used on Fedora.
- Pacman is used on Arch Linux.
- Keeping packages updated improves security.

---

# Interview Questions

1. What is a package?
2. What is a package manager?
3. Which package manager does Ubuntu use?
4. What is the purpose of `apt update`?
5. What is the difference between `apt remove` and `apt purge`?

---

# Next Topic

➡️ **17-Environment-Variables.md**
