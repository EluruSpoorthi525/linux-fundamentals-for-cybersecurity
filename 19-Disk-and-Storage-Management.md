# Disk and Storage Management

## Introduction

Disk and storage management is an essential Linux administration skill. It involves monitoring disk usage, managing partitions, mounting file systems, and maintaining storage devices efficiently. Proper storage management ensures optimal system performance and prevents data loss.

---

# Why is Disk Management Important?

Disk management helps to:

- Monitor storage usage
- Prevent disk space issues
- Manage partitions
- Mount storage devices
- Create backups
- Improve system performance

---

# Check Disk Space

Display disk usage:

```bash
df -h
```

Options:

- `-h` : Human-readable format

---

# Check Directory Size

Display directory size:

```bash
du -sh Documents/
```

Options:

- `-s` : Summary
- `-h` : Human-readable

---

# List Storage Devices

View all disks and partitions:

```bash
lsblk
```

Detailed disk information:

```bash
sudo fdisk -l
```

---

# Mount a File System

Mount a partition:

```bash
sudo mount /dev/sdb1 /mnt
```

Verify mounted devices:

```bash
mount
```

---

# Unmount a File System

Unmount a partition:

```bash
sudo umount /mnt
```

or

```bash
sudo umount /dev/sdb1
```

---

# Check Disk Usage

Display file system usage:

```bash
df -Th
```

Display inode usage:

```bash
df -i
```

---

# Create a File System

Format a partition with ext4:

```bash
sudo mkfs.ext4 /dev/sdb1
```

> **Warning:** Formatting erases all existing data on the partition.

---

# Disk Utilities

| Command | Purpose |
|----------|---------|
| `df` | Display disk space usage |
| `du` | Display directory/file size |
| `lsblk` | List block devices |
| `fdisk` | Manage disk partitions |
| `mount` | Mount a file system |
| `umount` | Unmount a file system |
| `mkfs` | Create a file system |

---

# Best Practices

- Monitor disk usage regularly.
- Remove unnecessary files.
- Keep backups of important data.
- Verify mounted devices before use.
- Avoid filling the root (`/`) partition completely.

---

# Cybersecurity Relevance

Proper disk management helps security professionals to:

- Secure sensitive data
- Monitor storage usage
- Preserve forensic evidence
- Manage backup storage
- Prevent denial-of-service caused by full disks

---

# Key Takeaways

- `df` checks disk usage.
- `du` displays directory sizes.
- `lsblk` lists storage devices.
- `mount` and `umount` manage file systems.
- `mkfs` creates a new file system.

---

# Interview Questions

1. What is the difference between `df` and `du`?
2. Which command lists storage devices?
3. How do you mount a partition?
4. What does `mkfs` do?
5. Why is disk management important?

---

# Next Topic

➡️ **20-Shell-Scripting-Basics.md**
```
