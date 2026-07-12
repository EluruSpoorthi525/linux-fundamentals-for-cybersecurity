# Text Processing Commands

## Introduction

Linux provides a rich set of command-line utilities for processing and manipulating text. These tools allow users to search, filter, sort, count, extract, and modify text efficiently without using a graphical editor.

Text processing commands are widely used in system administration, software development, and cybersecurity for tasks such as log analysis, searching configuration files, extracting information, and automating repetitive operations.

---

# Why Learn Text Processing?

Text processing helps you:

* Search log files
* Filter command output
* Count words and lines
* Extract specific fields
* Modify text
* Analyze large files
* Automate repetitive tasks

These skills are essential for Linux administration and cybersecurity.

---

# 1. cat

Displays the contents of a file.

### Syntax

```bash
cat filename
```

Example:

```bash
cat notes.txt
```

Combine multiple files:

```bash
cat file1.txt file2.txt
```

---

# 2. more

Displays file contents one page at a time.

```bash
more notes.txt
```

Useful for reading large files.

---

# 3. less

Displays large files interactively.

```bash
less notes.txt
```

Navigation:

* Up Arrow
* Down Arrow
* Page Up
* Page Down
* Press **q** to quit.

---

# 4. grep

Searches for text within files.

### Syntax

```bash
grep "text" filename
```

Example:

```bash
grep "error" logfile.txt
```

Ignore case:

```bash
grep -i "linux" notes.txt
```

Show line numbers:

```bash
grep -n "admin" users.txt
```

Search recursively:

```bash
grep -r "password" .
```

---

# 5. sort

Sorts lines alphabetically.

Example:

```bash
sort names.txt
```

Reverse order:

```bash
sort -r names.txt
```

Numeric sort:

```bash
sort -n numbers.txt
```

---

# 6. uniq

Removes duplicate lines.

Example:

```bash
uniq names.txt
```

Count duplicates:

```bash
uniq -c names.txt
```

> Note: `uniq` works best on sorted input.

---

# 7. wc (Word Count)

Counts lines, words, and characters.

Example:

```bash
wc notes.txt
```

Count lines:

```bash
wc -l notes.txt
```

Count words:

```bash
wc -w notes.txt
```

Count characters:

```bash
wc -c notes.txt
```

---

# 8. cut

Extracts selected columns from text.

Example:

```bash
cut -d ":" -f1 /etc/passwd
```

Options:

* `-d` → Delimiter
* `-f` → Field number

---

# 9. tr

Translates or replaces characters.

Convert lowercase to uppercase:

```bash
echo "linux" | tr 'a-z' 'A-Z'
```

Output:

```text
LINUX
```

---

# 10. sed (Stream Editor)

Edits text without opening a file.

Replace a word:

```bash
sed 's/Linux/Ubuntu/' notes.txt
```

Replace all occurrences:

```bash
sed 's/Linux/Ubuntu/g' notes.txt
```

---

# 11. awk

Processes structured text.

Display first column:

```bash
awk '{print $1}' data.txt
```

Display first and third columns:

```bash
awk '{print $1, $3}' data.txt
```

---

# 12. paste

Combines lines from multiple files.

```bash
paste file1.txt file2.txt
```

---

# 13. tee

Displays output and saves it to a file simultaneously.

Example:

```bash
echo "Hello Linux" | tee output.txt
```

Append to a file:

```bash
echo "Another Line" | tee -a output.txt
```

---

# 14. xargs

Builds and executes commands from standard input.

Example:

```bash
cat files.txt | xargs rm
```

---

# Command Summary

| Command | Purpose                            |
| ------- | ---------------------------------- |
| `cat`   | Display file contents              |
| `more`  | View file page by page             |
| `less`  | Interactive file viewer            |
| `grep`  | Search text                        |
| `sort`  | Sort lines                         |
| `uniq`  | Remove duplicates                  |
| `wc`    | Count lines, words, and characters |
| `cut`   | Extract fields                     |
| `tr`    | Translate characters               |
| `sed`   | Edit text                          |
| `awk`   | Process structured text            |
| `paste` | Merge files                        |
| `tee`   | Display and save output            |
| `xargs` | Build commands from input          |

---

# Practical Examples

Search failed login attempts:

```bash
grep "Failed" auth.log
```

Count users:

```bash
wc -l users.txt
```

Sort usernames:

```bash
sort users.txt
```

Display usernames from `/etc/passwd`:

```bash
cut -d ":" -f1 /etc/passwd
```

Convert text to uppercase:

```bash
echo "cybersecurity" | tr 'a-z' 'A-Z'
```

---

# Cybersecurity Relevance

Text processing commands are widely used for:

* Log analysis
* Incident response
* Threat hunting
* Malware analysis
* Configuration review
* User account auditing
* Security monitoring

Example:

```bash
grep "Failed password" /var/log/auth.log
```

This command helps identify failed SSH login attempts.

---

# Best Practices

* Use `grep` to quickly locate important information.
* Combine commands using pipes (`|`) for efficient workflows.
* Always verify the output before modifying files with `sed`.
* Learn `awk` gradually—it is a powerful text-processing tool.
* Practice with real log files whenever possible.

---

# Key Takeaways

* Linux offers powerful tools for processing text.
* `grep`, `sed`, and `awk` are essential commands for cybersecurity professionals.
* Text-processing commands save time when analyzing large files.
* Combining commands allows you to automate complex tasks.

---

# Interview Questions

1. What is the purpose of the `grep` command?
2. How do you ignore case while searching with `grep`?
3. What does the `sort` command do?
4. What is the difference between `more` and `less`?
5. What is the purpose of the `wc` command?
6. How does `cut` extract data?
7. What is `sed` used for?
8. What is the purpose of the `awk` command?
9. What does the `tee` command do?
10. Why are text-processing commands important in cybersecurity?

---

# Next Topic

➡️ **11-Searching-and-Finding-Files.md** – Learn how to locate files, directories, and executables using commands such as `find`, `locate`, `which`, and `whereis`, along with practical cybersecurity use cases.

