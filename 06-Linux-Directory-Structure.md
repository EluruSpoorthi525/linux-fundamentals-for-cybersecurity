# Linux Directory Structure

## Introduction

The Linux directory structure organizes files and folders in a hierarchical manner. Every file and directory begins from the **root directory (`/`)**, forming a tree-like structure.

Unlike Windows, Linux does not use drive letters such as `C:` or `D:`. Instead, all storage devices, partitions, and removable media are mounted under the root directory.

Understanding the directory structure is essential for navigating the system, locating files, managing applications, and performing cybersecurity tasks.

---

# What is a Directory?

A **directory** is a special type of file that stores references to other files and directories.

Directories help organize data into logical locations, making it easier to find and manage files.

Example:

```text
/home/student/Documents
```

Here:

* `home` is a directory.
* `student` is a subdirectory.
* `Documents` is another subdirectory.

---

# Linux Directory Tree

```text
/
├── bin
├── boot
├── dev
├── etc
├── home
│   ├── alice
│   ├── bob
│   └── student
├── lib
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── srv
├── sys
├── tmp
├── usr
└── var
```

Every directory has a specific purpose.

---

# Important Directories

## `/`

The root directory.

Everything starts here.

---

## `/home`

Stores personal files for regular users.

Example:

```text
/home/student
```

---

## `/root`

Home directory of the root (administrator) user.

---

## `/etc`

Contains configuration files.

Examples:

* Network configuration
* User accounts
* System services

---

## `/var`

Stores changing data such as:

* Logs
* Mail
* Cache
* Databases

---

## `/tmp`

Temporary storage for applications.

Files may be deleted automatically after reboot.

---

## `/usr`

Contains applications and shared resources.

Examples:

* Programs
* Libraries
* Documentation

---

## `/bin`

Stores essential user commands.

Examples:

* ls
* cp
* mv
* cat

---

## `/sbin`

Contains administrative commands.

Examples:

* reboot
* shutdown
* fsck

---

## `/dev`

Contains device files.

Examples:

* Hard disks
* USB drives
* Printers

---

## `/proc`

Virtual directory containing process information.

Useful for system monitoring.

---

# Navigation Commands

## `pwd`

Displays the current working directory.

Example:

```bash
pwd
```

Output:

```text
/home/student
```

---

## `ls`

Lists files and directories.

Example:

```bash
ls
```

Common options:

```bash
ls -l
ls -a
ls -lh
```

---

## `cd`

Changes the current directory.

Example:

```bash
cd Documents
```

Move to the home directory:

```bash
cd
```

Move to the previous directory:

```bash
cd ..
```

Move to the root directory:

```bash
cd /
```

---

# Special Directory Symbols

| Symbol | Meaning           |
| ------ | ----------------- |
| `.`    | Current directory |
| `..`   | Parent directory  |
| `~`    | Home directory    |
| `/`    | Root directory    |

Examples:

```bash
cd ~
cd ..
cd .
```

---

# Absolute Path

An absolute path starts from the root directory.

Example:

```text
/home/student/Documents/report.txt
```

It always begins with `/`.

---

# Relative Path

A relative path starts from the current directory.

Example:

```text
Documents/report.txt
```

It does not begin with `/`.

---

# Hidden Files

Hidden files begin with a period (`.`).

Examples:

```text
.bashrc
.profile
.gitconfig
```

To view hidden files:

```bash
ls -a
```

---

# Viewing Directory Contents

Long listing:

```bash
ls -l
```

Human-readable sizes:

```bash
ls -lh
```

Recursive listing:

```bash
ls -R
```

---

# Displaying the Directory Tree

Some Linux distributions include the `tree` command.

Example:

```bash
tree
```

Output:

```text
Documents
├── Notes
├── Projects
└── Images
```

---

# Why Directory Structure Matters in Cybersecurity

Cybersecurity professionals frequently navigate Linux systems to:

* Find log files
* Locate configuration files
* Investigate malware
* Review user data
* Collect forensic evidence
* Analyze compromised systems

Efficient navigation saves time during investigations.

---

# Best Practices

* Keep personal files inside your home directory.
* Avoid modifying system directories without permission.
* Learn navigation shortcuts.
* Use absolute paths for critical operations.
* Verify your current directory before executing commands.

---

# Key Takeaways

* Linux uses a hierarchical directory structure.
* The root directory (`/`) is the top-level directory.
* Navigation is performed using commands such as `pwd`, `ls`, and `cd`.
* Hidden files begin with a period (`.`).
* Understanding the directory structure is essential for Linux administration and cybersecurity.

---

# Interview Questions

1. What is the root directory in Linux?
2. What is the purpose of the `/home` directory?
3. What does the `pwd` command do?
4. How do you list hidden files?
5. What is the difference between an absolute path and a relative path?
6. What does `cd ..` do?
7. What is the purpose of the `/etc` directory?
8. Why are hidden files used?
9. What is the difference between `/home` and `/root`?
10. Why is understanding the Linux directory structure important for cybersecurity?

---

# Next Topic

➡️ **07-Linux-Terminal-and-Shell.md** – Learn about the Linux terminal, different types of shells, the Bash shell, command syntax, and how users interact with the Linux operating system using the command-line interface.

