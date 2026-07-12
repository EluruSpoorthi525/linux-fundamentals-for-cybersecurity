# Working with Files and Directories

## Introduction

Files and directories are fundamental components of every Linux system. Whether you are a system administrator, developer, or cybersecurity professional, managing files and directories is a daily task.

Linux provides powerful commands to create, copy, move, rename, delete, search, and organize files efficiently through the command line.

In this chapter, you'll learn the essential commands used to manage files and directories.

---

# What is a File?

A **file** is a collection of data stored on a storage device.

Examples include:

* Text files
* Images
* Videos
* Documents
* Programs
* Configuration files

Example:

```text
notes.txt
report.pdf
photo.jpg
```

---

# What is a Directory?

A **directory** (folder) is used to organize files and other directories.

Example:

```text
Documents/
Projects/
Downloads/
Pictures/
```

Directories make it easier to manage files.

---

# Creating Files

## touch

Creates an empty file.

### Syntax

```bash
touch filename
```

### Example

```bash
touch notes.txt
```

Create multiple files:

```bash
touch file1.txt file2.txt file3.txt
```

---

# Viewing File Contents

## cat

Displays the contents of a file.

### Syntax

```bash
cat filename
```

Example:

```bash
cat notes.txt
```

---

## less

Displays file contents one page at a time.

```bash
less notes.txt
```

Useful for reading large files.

Press **q** to exit.

---

## head

Displays the first 10 lines.

```bash
head notes.txt
```

Display first 5 lines:

```bash
head -5 notes.txt
```

---

## tail

Displays the last 10 lines.

```bash
tail notes.txt
```

Display last 20 lines:

```bash
tail -20 notes.txt
```

Monitor a growing log file:

```bash
tail -f /var/log/syslog
```

---

# Creating Directories

## mkdir

Creates directories.

### Syntax

```bash
mkdir directory_name
```

Example:

```bash
mkdir Projects
```

Create multiple directories:

```bash
mkdir Docs Images Videos
```

Create nested directories:

```bash
mkdir -p Projects/Linux/Notes
```

---

# Copying Files

## cp

Copies files.

### Syntax

```bash
cp source destination
```

Example:

```bash
cp notes.txt backup.txt
```

Copy a directory:

```bash
cp -r Projects Backup
```

---

# Moving and Renaming Files

## mv

Moves or renames files.

Rename:

```bash
mv old.txt new.txt
```

Move:

```bash
mv notes.txt Documents/
```

Move and rename:

```bash
mv report.txt Documents/final-report.txt
```

---

# Deleting Files

## rm

Deletes files.

```bash
rm notes.txt
```

Delete multiple files:

```bash
rm file1.txt file2.txt
```

Delete without confirmation:

```bash
rm -f notes.txt
```

---

# Deleting Directories

Delete an empty directory:

```bash
rmdir EmptyFolder
```

Delete a directory and all its contents:

```bash
rm -r Projects
```

Force delete:

```bash
rm -rf Projects
```

> **Warning:** `rm -rf` permanently deletes files and directories. Use it carefully.

---

# Displaying File Information

## file

Identifies the file type.

```bash
file notes.txt
```

Example output:

```text
notes.txt: ASCII text
```

---

# Displaying File Size

```bash
ls -lh
```

Human-readable file sizes.

---

## du

Displays disk usage.

```bash
du -h
```

Display folder size:

```bash
du -sh Documents
```

---

# Finding Files

## find

Searches for files and directories.

Example:

```bash
find /home -name notes.txt
```

Search directories:

```bash
find . -type d
```

Search files:

```bash
find . -type f
```

---

# Locating Commands

## which

Shows the location of a command.

```bash
which python
```

Example:

```text
/usr/bin/python
```

---

# Wildcards

Linux supports wildcard characters.

| Wildcard | Meaning                          |
| -------- | -------------------------------- |
| `*`      | Matches any number of characters |
| `?`      | Matches a single character       |
| `[ ]`    | Matches a character from a set   |

Example:

```bash
ls *.txt
```

Lists all text files.

---

# File Management Workflow

```text
Create File
      │
      ▼
View File
      │
      ▼
Copy File
      │
      ▼
Move/Rename File
      │
      ▼
Delete File
```

---

# Cybersecurity Relevance

File management skills are essential for cybersecurity tasks such as:

* Locating malware samples
* Managing log files
* Organizing forensic evidence
* Backing up configuration files
* Reviewing security reports
* Investigating compromised systems

---

# Best Practices

* Verify file names before deleting.
* Use `rm -rf` only when absolutely necessary.
* Keep important files backed up.
* Organize files into meaningful directories.
* Use descriptive file names.

---

# Key Takeaways

* Linux provides powerful commands for managing files and directories.
* `touch` creates files.
* `mkdir` creates directories.
* `cp` copies files.
* `mv` moves and renames files.
* `rm` deletes files.
* `find` searches for files.
* Proper file management is essential for Linux administration and cybersecurity.

---

# Interview Questions

1. What is the difference between a file and a directory?
2. How do you create an empty file?
3. What is the difference between `cp` and `mv`?
4. How do you delete an empty directory?
5. What does `rm -rf` do?
6. Which command displays the first 10 lines of a file?
7. Which command displays the last 10 lines?
8. How do you search for a file in Linux?
9. What are wildcards used for?
10. Why is file management important in cybersecurity?

---

# Next Topic

➡️ **10-Text-Processing-Commands.md** – Learn how to view, search, filter, sort, count, and manipulate text using powerful Linux commands such as `grep`, `sort`, `wc`, `cut`, `awk`, and `sed`.

