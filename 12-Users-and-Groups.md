# Linux Users and Groups

## Introduction

Linux is a **multi-user operating system**, meaning multiple users can access the same system simultaneously. To maintain security and organize access, Linux uses **users** and **groups**. Every file, process, and service is associated with a user and often a group.

Understanding users and groups is fundamental for Linux administration, cybersecurity, and system management. Proper user management helps enforce the **Principle of Least Privilege**, reducing the risk of unauthorized access.

---

# What is a User?

A **user** is an account that allows a person or service to log in and interact with the Linux system.

Each user has:

* Username
* User ID (UID)
* Home directory
* Default shell
* Password (stored securely)
* Group membership

Example users:

```text
alice
bob
student
root
```

---

# Types of Users

## 1. Root User

The **root** user is the administrator of the Linux system.

Characteristics:

* UID = 0
* Full control over the system
* Can access all files
* Can install or remove software
* Can create or delete users
* Should be used cautiously

---

## 2. Regular Users

Regular users perform everyday tasks.

Examples:

* Browsing files
* Running applications
* Writing documents
* Executing permitted commands

Regular users have limited permissions.

---

## 3. System Users

System users are created automatically for running services and applications.

Examples:

* `www-data`
* `mysql`
* `sshd`
* `nobody`

These accounts usually cannot log in interactively.

---

# What is a Group?

A **group** is a collection of users who share common permissions.

Groups simplify permission management by allowing administrators to assign permissions to multiple users at once.

Example:

```text
developers
admins
students
```

---

# Primary Group vs Secondary Group

Each user has:

### Primary Group

The default group assigned when the user is created.

### Secondary Groups

Additional groups that grant extra permissions.

Example:

```text
User: alice

Primary Group:
developers

Secondary Groups:
docker
sudo
security
```

---

# Important User Files

## `/etc/passwd`

Stores user account information.

Example:

```text
student:x:1000:1000:Student User:/home/student:/bin/bash
```

Fields:

1. Username
2. Password placeholder
3. User ID (UID)
4. Group ID (GID)
5. User description
6. Home directory
7. Login shell

---

## `/etc/shadow`

Stores encrypted user passwords and password policies.

Only the root user can access this file.

---

## `/etc/group`

Stores information about groups.

Example:

```text
developers:x:1001:alice,bob
```

---

# Viewing User Information

## whoami

Displays the current user.

```bash
whoami
```

---

## id

Displays user and group information.

```bash
id
```

Example output:

```text
uid=1000(student) gid=1000(student) groups=1000(student),27(sudo)
```

---

## who

Shows users currently logged in.

```bash
who
```

---

## groups

Displays the groups a user belongs to.

```bash
groups
```

---

# Creating Users

## useradd

Creates a new user.

Syntax:

```bash
sudo useradd username
```

Example:

```bash
sudo useradd john
```

Create a home directory:

```bash
sudo useradd -m john
```

Specify the default shell:

```bash
sudo useradd -m -s /bin/bash john
```

---

# Setting a Password

Use the `passwd` command:

```bash
sudo passwd john
```

The system will prompt for a new password.

---

# Deleting Users

Delete a user:

```bash
sudo userdel john
```

Delete the user and their home directory:

```bash
sudo userdel -r john
```

---

# Modifying Users

Change a username:

```bash
sudo usermod -l newname oldname
```

Lock a user account:

```bash
sudo usermod -L john
```

Unlock a user account:

```bash
sudo usermod -U john
```

---

# Managing Groups

## groupadd

Create a group:

```bash
sudo groupadd developers
```

---

## groupdel

Delete a group:

```bash
sudo groupdel developers
```

---

## Add User to a Group

```bash
sudo usermod -aG developers john
```

> **Note:** Always use the `-aG` option together. Omitting `-a` can remove the user from other supplementary groups.

---

## Remove User from a Group

```bash
sudo gpasswd -d john developers
```

---

# The sudo Command

The **sudo** command allows authorized users to execute commands with administrative privileges.

Example:

```bash
sudo apt update
```

Users who need administrative access are typically members of the `sudo` group (or the `wheel` group on some distributions).

---

# Switching Users

Switch to another user:

```bash
su john
```

Switch to the root user:

```bash
sudo su
```

Return to the previous user:

```bash
exit
```

---

# User Management Workflow

```text
Create User
      │
      ▼
Set Password
      │
      ▼
Assign Groups
      │
      ▼
Grant Permissions
      │
      ▼
Manage Account
```

---

# Best Practices

* Create separate accounts for each user.
* Avoid logging in directly as the root user.
* Use `sudo` instead of working as root.
* Follow the Principle of Least Privilege.
* Remove unused user accounts.
* Review group memberships regularly.
* Use strong passwords and password policies.

---

# Cybersecurity Relevance

Managing users and groups is a key part of securing Linux systems.

Cybersecurity professionals use these skills to:

* Create secure user accounts
* Limit user privileges
* Prevent unauthorized access
* Audit group memberships
* Investigate compromised accounts
* Enforce access control policies

Proper user management reduces the attack surface and helps maintain system integrity.

---

# Key Takeaways

* Linux is a multi-user operating system.
* Every user has a unique UID and belongs to one or more groups.
* The root user has complete control over the system.
* `useradd`, `usermod`, and `userdel` manage user accounts.
* `groupadd` and `groupdel` manage groups.
* `sudo` provides temporary administrative privileges.
* Following the Principle of Least Privilege improves system security.

---

# Interview Questions

1. What is the difference between the root user and a regular user?
2. What is a Linux group?
3. What is the purpose of the `/etc/passwd` file?
4. Why is `/etc/shadow` protected?
5. What is the difference between a primary group and a secondary group?
6. How do you create a new user with a home directory?
7. How do you add a user to a group?
8. What is the purpose of the `sudo` command?
9. What command displays the current user's identity and group information?
10. Why is user and group management important in cybersecurity?

---

# Hands-on Practice

Run the following commands in a Linux virtual machine:

```bash
whoami
id
groups

sudo useradd -m demo_user
sudo passwd demo_user

sudo groupadd developers
sudo usermod -aG developers demo_user

id demo_user

sudo userdel -r demo_user
sudo groupdel developers
```

Observe how users and groups are created, modified, and removed.

---

# Next Topic

➡️ **13-Linux-File-Permissions.md** – Learn how Linux controls access to files and directories using ownership, permissions, `chmod`, `chown`, `umask`, and special permissions such as SUID, SGID, and the Sticky Bit.

