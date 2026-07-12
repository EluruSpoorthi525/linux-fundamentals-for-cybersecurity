# Linux File Permissions

## Introduction

Linux is a multi-user operating system, meaning multiple users can access the same system simultaneously. To protect files and directories from unauthorized access, Linux uses a **permission-based security model**.

Every file and directory has an owner, a group, and a set of permissions that determine who can read, write, or execute it.

Understanding file permissions is essential for Linux administration, cybersecurity, penetration testing, digital forensics, and system hardening.

---

# Why File Permissions Matter

File permissions help:

* Protect sensitive information
* Prevent unauthorized modifications
* Control user access
* Secure system files
* Reduce security risks
* Maintain system integrity

---

# File Ownership

Every file has three ownership attributes:

* **User (Owner):** The person who owns the file.
* **Group:** A collection of users with shared permissions.
* **Others:** Everyone else on the system.

Example:

```bash
ls -l notes.txt
```

Output:

```text
-rw-r--r-- 1 student developers 1024 Jul 12 10:30 notes.txt
```

Breakdown:

```text
-rw-r--r--
││ │ │
││ │ └── Others
││ └──── Group
│└────── Owner
└──────── File Type
```

---

# File Types

The first character indicates the file type.

| Symbol | File Type         |
| ------ | ----------------- |
| `-`    | Regular File      |
| `d`    | Directory         |
| `l`    | Symbolic Link     |
| `c`    | Character Device  |
| `b`    | Block Device      |
| `s`    | Socket            |
| `p`    | Named Pipe (FIFO) |

Example:

```text
drwxr-xr-x
```

The **d** indicates a directory.

---

# Permission Types

Linux has three basic permissions.

| Symbol | Permission | Meaning                              |
| ------ | ---------- | ------------------------------------ |
| `r`    | Read       | View file contents or list directory |
| `w`    | Write      | Modify a file or directory           |
| `x`    | Execute    | Run a file or enter a directory      |

---

# Permission Structure

Example:

```text
-rwxr-xr--
```

Breakdown:

```text
File Type

-

Owner

rwx

Group

r-x

Others

r--
```

Meaning:

* Owner: Read, Write, Execute
* Group: Read, Execute
* Others: Read only

---

# Numeric Permission Values

Each permission has a numeric value.

| Permission  | Value |
| ----------- | ----: |
| Read (r)    |     4 |
| Write (w)   |     2 |
| Execute (x) |     1 |

Examples:

| Number | Permission |
| ------ | ---------- |
| 7      | rwx        |
| 6      | rw-        |
| 5      | r-x        |
| 4      | r--        |
| 0      | ---        |

Common permission sets:

| Numeric | Symbolic  |
| ------- | --------- |
| 777     | rwxrwxrwx |
| 755     | rwxr-xr-x |
| 700     | rwx------ |
| 644     | rw-r--r-- |
| 600     | rw------- |

---

# chmod

The **chmod** command changes file permissions.

### Symbolic Mode

Add execute permission:

```bash
chmod +x script.sh
```

Remove write permission:

```bash
chmod -w notes.txt
```

Grant read permission to the group:

```bash
chmod g+r report.txt
```

---

### Numeric Mode

Set permissions to **755**:

```bash
chmod 755 script.sh
```

Set permissions to **644**:

```bash
chmod 644 notes.txt
```

Set permissions to **600**:

```bash
chmod 600 secrets.txt
```

---

# chown

Changes the owner of a file.

Syntax:

```bash
sudo chown user filename
```

Example:

```bash
sudo chown alice report.txt
```

Change owner and group:

```bash
sudo chown alice:developers report.txt
```

---

# chgrp

Changes the group ownership.

Example:

```bash
sudo chgrp developers report.txt
```

---

# umask

The **umask** determines the default permissions for newly created files and directories.

View the current umask:

```bash
umask
```

Example output:

```text
0022
```

A common default umask of `022` results in:

* New files: `644`
* New directories: `755`

---

# Special Permissions

## SUID (Set User ID)

Allows a program to run with the permissions of the file owner.

Example:

```bash
chmod u+s program
```

Symbol:

```text
rws
```

---

## SGID (Set Group ID)

Files run with the group's permissions. On directories, new files inherit the directory's group.

```bash
chmod g+s directory
```

---

## Sticky Bit

Prevents users from deleting files they do not own within a shared directory.

Commonly used on:

```text
/tmp
```

Set the Sticky Bit:

```bash
chmod +t shared_directory
```

---

# Viewing Permissions

Long listing format:

```bash
ls -l
```

Detailed information:

```bash
stat filename
```

---

# Best Practices

* Apply the **principle of least privilege**.
* Avoid using `777` unless absolutely necessary.
* Protect sensitive files with `600` permissions.
* Review permissions regularly.
* Limit the use of root privileges.

---

# Cybersecurity Relevance

File permissions are critical in cybersecurity for:

* Securing sensitive data
* Preventing privilege escalation
* Protecting configuration files
* Controlling access to logs
* Hardening Linux servers
* Auditing system security

Example:

Restrict access to an SSH private key:

```bash
chmod 600 ~/.ssh/id_rsa
```

This ensures only the owner can read and modify the file.

---

# Key Takeaways

* Linux uses permissions to control access to files and directories.
* Every file has an owner, a group, and permissions for others.
* `chmod` changes permissions.
* `chown` changes file ownership.
* `chgrp` changes group ownership.
* `umask` defines default permissions.
* Special permissions (SUID, SGID, Sticky Bit) provide advanced access control.

---

# Interview Questions

1. What are the three basic Linux file permissions?
2. What do the numbers `755` and `644` represent?
3. What is the difference between `chmod` and `chown`?
4. What does the `umask` command do?
5. What is the purpose of the Sticky Bit?
6. What is SUID?
7. What is SGID?
8. Why is `777` considered insecure?
9. How do you change the owner of a file?
10. Why are file permissions important in cybersecurity?

---

# Hands-on Practice

Run the following commands in a Linux terminal:

```bash
touch demo.txt
ls -l demo.txt

chmod 644 demo.txt
chmod 600 demo.txt
chmod +x demo.txt

mkdir shared
chmod 755 shared

ls -l
stat demo.txt
```

Observe how the permissions change after each command.

---

# Next Topic

➡️ **13-Linux-Users-and-Groups.md** – Learn how Linux manages users and groups, create and delete user accounts, assign group memberships, configure passwords, and understand the role of root and sudo in system administration.

