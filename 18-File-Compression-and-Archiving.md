# File Compression and Archiving

## Introduction

File compression and archiving are essential Linux skills used to reduce file size, save storage space, speed up file transfers, and create backups. While **archiving** combines multiple files into a single file, **compression** reduces the size of that file.

Linux provides several built-in tools for archiving and compressing files.

---

# Archiving vs Compression

| Archiving | Compression |
|------------|-------------|
| Combines multiple files into one | Reduces file size |
| Uses `tar` | Uses `gzip`, `bzip2`, `xz` |
| Does not reduce size by itself | Makes files smaller |

---

# Common Compression Formats

| Format | Extension | Command |
|---------|-----------|---------|
| TAR | `.tar` | `tar` |
| Gzip | `.gz` | `gzip` |
| Bzip2 | `.bz2` | `bzip2` |
| XZ | `.xz` | `xz` |
| ZIP | `.zip` | `zip` |

---

# tar Command

Create an archive:

```bash
tar -cvf archive.tar folder/
```

Extract an archive:

```bash
tar -xvf archive.tar
```

View archive contents:

```bash
tar -tvf archive.tar
```

---

# gzip Command

Compress a file:

```bash
gzip file.txt
```

Decompress:

```bash
gunzip file.txt.gz
```

---

# bzip2 Command

Compress:

```bash
bzip2 file.txt
```

Decompress:

```bash
bunzip2 file.txt.bz2
```

---

# xz Command

Compress:

```bash
xz file.txt
```

Decompress:

```bash
unxz file.txt.xz
```

---

# zip Command

Create a ZIP archive:

```bash
zip -r archive.zip folder/
```

Extract a ZIP archive:

```bash
unzip archive.zip
```

---

# Combining tar and gzip

Create a compressed archive:

```bash
tar -czvf backup.tar.gz folder/
```

Extract:

```bash
tar -xzvf backup.tar.gz
```

---

# Best Practices

- Compress large files before sharing.
- Archive important files before backup.
- Verify archives after creation.
- Use meaningful archive names.
- Store backups in a secure location.

---

# Cybersecurity Relevance

Compression and archiving are commonly used to:

- Create secure backups
- Archive log files
- Transfer forensic evidence
- Store system snapshots
- Reduce storage usage

Security professionals frequently archive logs before analysis or incident response.

---

# Key Takeaways

- Archiving combines multiple files into one.
- Compression reduces file size.
- `tar` is used for archiving.
- `gzip`, `bzip2`, and `xz` compress files.
- `zip` creates cross-platform archives.

---

# Interview Questions

1. What is the difference between archiving and compression?
2. Which command creates a TAR archive?
3. How do you extract a `.tar.gz` file?
4. What does the `gzip` command do?
5. Why is file compression important?

---

# Next Topic

➡️ **19-Disk-and-Storage-Management.md**
```
