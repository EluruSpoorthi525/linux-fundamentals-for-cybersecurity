# Linux File System

## Introduction

The **Linux File System** is the method Linux uses to organize, store, retrieve, and manage data on storage devices. Unlike Windows, which uses separate drive letters such as `C:` and `D:`, Linux organizes everything under a single directory called the **root directory (`/`)**.

In Linux, everything is treated as a file. This includes regular files, directories, hardware devices, and many system resources.

Understanding the Linux file system is essential for system administration and cybersecurity because it helps you locate important files, configure systems, analyze logs, and manage permissions.

---

# What is a File System?

A **file system** is a structure that determines how files and directories are stored and organized on a storage device.

It is responsible for:

* Organizing files and folders
* Managing storage space
* Controlling file access
* Storing file metadata
* Ensuring data integrity

Without a file system, the operating system would not know where files are stored.

---

# Root Directory (/)

The **root directory (`/`)** is the top-level directory in Linux.

Every file and directory originates from the root directory.

Example:

```text
/
├── bin
├── boot
├── dev
├── etc
├── home
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

---

# Linux File System Hierarchy

Linux follows the **Filesystem Hierarchy Standard (FHS)**, which defines where files and directories should be located.

This standard ensures consistency across Linux distributions.

---

# Important Directories

## `/bin`

Contains essential user commands.

Examples:

* ls
* cp
* mv
* cat
* pwd

---

## `/boot`

Contains files required to boot Linux.

Includes:

* Linux kernel
* Bootloader files
* Initial RAM disk

---

## `/dev`

Contains device files.

Examples:

* Hard disks
* USB drives
* Printers
* Keyboard
* Mouse

Linux treats hardware devices as files.

---

## `/etc`

Stores system-wide configuration files.

Examples:

* User account information
* Network configuration
* Service configuration

System administrators frequently work in this directory.

---

## `/home`

Contains personal directories for users.

Example:

```text
/home/alice
/home/bob
```

Each user stores personal files here.

---

## `/lib`

Contains shared libraries required by programs and the kernel.

---

## `/media`

Used for automatically mounted removable media.

Examples:

* USB drives
* DVDs
* External storage

---

## `/mnt`

Used for temporarily mounting storage devices.

---

## `/opt`

Contains optional third-party software.

---

## `/proc`

A virtual file system containing information about running processes and the kernel.

Useful for:

* System monitoring
* Process information
* Memory information

---

## `/root`

Home directory of the root (administrator) user.

---

## `/run`

Stores temporary runtime information.

---

## `/sbin`

Contains essential system administration commands.

Examples:

* fsck
* reboot
* shutdown

---

## `/srv`

Stores data for system services.

---

## `/sys`

Provides information about hardware and the Linux kernel.

---

## `/tmp`

Stores temporary files.

Files here may be deleted automatically after a reboot.

---

## `/usr`

Contains user applications and shared resources.

Subdirectories include:

* /usr/bin
* /usr/lib
* /usr/share

---

## `/var`

Stores files that change frequently.

Examples:

* Log files
* Mail
* Cache
* Databases

---

# File Types in Linux

Linux supports several file types.

| File Type         | Description                     |
| ----------------- | ------------------------------- |
| Regular File      | Stores data                     |
| Directory         | Organizes files                 |
| Symbolic Link     | Shortcut to another file        |
| Block Device      | Storage devices                 |
| Character Device  | Hardware devices                |
| Socket            | Communication between processes |
| Named Pipe (FIFO) | Data transfer between processes |

---

# Absolute vs Relative Paths

## Absolute Path

Starts from the root directory.

Example:

```text
/home/student/Documents/report.txt
```

---

## Relative Path

Starts from the current working directory.

Example:

```text
Documents/report.txt
```

---

# Inodes

An **inode** is a data structure that stores metadata about a file.

It contains information such as:

* File size
* Owner
* Permissions
* Creation time
* Modification time
* File location

Each file has a unique inode number.

---

# Mounting

Linux uses **mounting** to make storage devices accessible.

Examples include:

* Hard drives
* USB devices
* Network storage

Before a storage device can be used, it must be mounted to the file system.

---

# Common File Systems

| File System | Description                            |
| ----------- | -------------------------------------- |
| ext4        | Default Linux file system              |
| XFS         | High-performance file system           |
| Btrfs       | Advanced features such as snapshots    |
| FAT32       | Compatible with Windows and Linux      |
| NTFS        | Windows file system with Linux support |

---

# Why the Linux File System Matters in Cybersecurity

Cybersecurity professionals frequently interact with the file system to:

* Locate log files
* Analyze malware
* Investigate compromised systems
* Review configuration files
* Monitor system activity
* Recover evidence during digital forensics

Knowing where important files are stored speeds up investigations.

---

# Best Practices

* Keep system files organized.
* Avoid modifying system directories unnecessarily.
* Regularly back up important files.
* Protect sensitive files using proper permissions.
* Monitor storage usage.

---

# Key Takeaways

* Linux organizes everything under the root directory (`/`).
* Everything in Linux is treated as a file.
* The Filesystem Hierarchy Standard (FHS) defines directory organization.
* Understanding directories helps manage and secure Linux systems.
* Knowledge of the file system is essential for cybersecurity professionals.

---

# Interview Questions

1. What is the Linux file system?
2. What is the root directory?
3. What is the purpose of the `/etc` directory?
4. What information is stored in an inode?
5. What is the difference between an absolute path and a relative path?
6. What is mounting?
7. Name five important Linux directories and their purposes.
8. What are symbolic links?
9. Why is the `/var` directory important?
10. Why is understanding the Linux file system important in cybersecurity?

---

# Next Topic

➡️ **06-Linux-Directory-Structure.md** – Learn how to navigate the Linux directory structure, understand common directories in more detail, and use commands like `pwd`, `cd`, and `ls` to move around the file system efficiently.

