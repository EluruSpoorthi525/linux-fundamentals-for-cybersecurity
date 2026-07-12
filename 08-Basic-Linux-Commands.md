# Basic Linux Commands

## Introduction

Linux is primarily managed through the **Command-Line Interface (CLI)**. Commands allow users to interact with the operating system, manage files, retrieve system information, and perform administrative tasks efficiently.

This chapter introduces the most commonly used Linux commands that every beginner should know. Mastering these commands provides the foundation for system administration and cybersecurity.

---

# Command Syntax

Most Linux commands follow this format:

```bash
command [options] [arguments]
```

Example:

```bash
ls -l /home
```

* **Command:** `ls`
* **Option:** `-l`
* **Argument:** `/home`

---

# 1. `pwd` (Print Working Directory)

Displays the current directory.

### Syntax

```bash
pwd
```

### Example

```bash
$ pwd
/home/student
```

---

# 2. `ls` (List Directory Contents)

Displays files and directories.

### Syntax

```bash
ls
```

### Common Options

```bash
ls -l
```

Long listing format.

```bash
ls -a
```

Shows hidden files.

```bash
ls -lh
```

Human-readable file sizes.

```bash
ls -R
```

Recursive listing.

---

# 3. `cd` (Change Directory)

Changes the current directory.

### Examples

Go to home directory:

```bash
cd
```

Go to Documents:

```bash
cd Documents
```

Go to parent directory:

```bash
cd ..
```

Go to root directory:

```bash
cd /
```

Go to previous directory:

```bash
cd -
```

---

# 4. `clear`

Clears the terminal screen.

```bash
clear
```

Shortcut:

```text
Ctrl + L
```

---

# 5. `whoami`

Displays the current logged-in user.

```bash
whoami
```

Example:

```bash
student
```

---

# 6. `hostname`

Displays the system hostname.

```bash
hostname
```

Example:

```bash
ubuntu
```

---

# 7. `date`

Displays the current system date and time.

```bash
date
```

Example:

```text
Mon Jul 13 10:35:21 IST 2026
```

---

# 8. `cal`

Displays a calendar.

```bash
cal
```

Example:

```text
     July 2026
Su Mo Tu We Th Fr Sa
...
```

---

# 9. `uname`

Displays system information.

```bash
uname
```

Useful options:

```bash
uname -a
```

Shows all available system information.

---

# 10. `echo`

Prints text to the terminal.

```bash
echo "Hello Linux"
```

Output:

```text
Hello Linux
```

---

# 11. `man`

Displays the manual page for a command.

Example:

```bash
man ls
```

Use **q** to exit the manual.

---

# 12. `history`

Shows previously executed commands.

```bash
history
```

Useful for reviewing command history.

---

# 13. `exit`

Closes the current terminal session.

```bash
exit
```

---

# Command Summary

| Command    | Purpose                    |
| ---------- | -------------------------- |
| `pwd`      | Show current directory     |
| `ls`       | List files and directories |
| `cd`       | Change directory           |
| `clear`    | Clear terminal screen      |
| `whoami`   | Show current user          |
| `hostname` | Display computer name      |
| `date`     | Show current date and time |
| `cal`      | Display calendar           |
| `uname`    | Display system information |
| `echo`     | Print text                 |
| `man`      | View command manual        |
| `history`  | View command history       |
| `exit`     | Exit terminal              |

---

# Best Practices

* Practice commands every day.
* Read the manual page before using unfamiliar commands.
* Use the **Tab** key for auto-completion.
* Review your command history regularly.
* Avoid running commands as the root user unless necessary.

---

# Hands-on Practice

Try the following commands:

```bash
pwd
ls
ls -l
ls -a
cd /
pwd
cd ~
whoami
hostname
date
cal
uname -a
echo "Learning Linux"
history
```

Observe the output of each command and understand what it does.

---

# Key Takeaways

* Linux commands are powerful tools for interacting with the operating system.
* Understanding basic commands is essential before learning file management and system administration.
* The `man` command provides built-in documentation for most Linux commands.
* Regular practice is the best way to become comfortable with the Linux command line.

---

# Interview Questions

1. What is the purpose of the `pwd` command?
2. How do you display hidden files?
3. What does `cd ..` do?
4. What is the difference between `ls` and `ls -l`?
5. Which command displays the current logged-in user?
6. How do you display detailed system information?
7. What is the purpose of the `echo` command?
8. How do you access the manual page for a command?
9. Which command shows previously executed commands?
10. Why is practicing Linux commands important?

---

# Next Topic

➡️ **09-Working-with-Files-and-Directories.md** – Learn how to create, copy, move, rename, delete, and organize files and directories using essential Linux file management commands.

