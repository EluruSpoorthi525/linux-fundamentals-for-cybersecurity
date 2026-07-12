# 23-Input-Output-Redirection

## Introduction

Input and Output (I/O) Redirection allows you to control where a command receives its input and where it sends its output. Instead of displaying results on the terminal, you can save them to files, append data, or redirect errors.

I/O redirection is an essential Linux skill used in system administration, automation, and cybersecurity.

---

# Standard Streams

Linux has three standard streams:

| Stream | Description | Default |
|---------|-------------|---------|
| Standard Input (stdin) | Receives input | Keyboard |
| Standard Output (stdout) | Displays output | Terminal |
| Standard Error (stderr) | Displays error messages | Terminal |

---

# Output Redirection (`>`)

Redirect output to a file.

```bash
echo "Hello Linux" > output.txt
```

If the file doesn't exist, it is created. If it exists, its contents are overwritten.

---

# Append Output (`>>`)

Append output to the end of a file.

```bash
echo "Welcome" >> output.txt
```

---

# Input Redirection (`<`)

Read input from a file.

```bash
sort < names.txt
```

---

# Redirect Errors (`2>`)

Save error messages to a file.

```bash
ls invalidfile 2> error.txt
```

---

# Redirect Output and Errors

Save both output and errors.

```bash
command > output.txt 2>&1
```

---

# Discard Output

Send output to `/dev/null`.

```bash
ls invalidfile > /dev/null 2>&1
```

---

# Pipe (`|`)

A pipe sends the output of one command as the input to another.

Example:

```bash
ls -l | less
```

Count files:

```bash
ls | wc -l
```

Search text:

```bash
cat file.txt | grep "Linux"
```

---

# Common Redirection Operators

| Operator | Purpose |
|----------|---------|
| `>` | Overwrite output |
| `>>` | Append output |
| `<` | Read input |
| `2>` | Redirect errors |
| `|` | Pipe output |
| `/dev/null` | Discard output |

---

# Best Practices

- Use `>>` when you don't want to overwrite files.
- Save error logs separately for troubleshooting.
- Use pipes to combine commands efficiently.
- Redirect unnecessary output to `/dev/null`.

---

# Cybersecurity Relevance

Input and Output Redirection is commonly used to:

- Save scan results
- Store log files
- Filter command output
- Analyze security logs
- Automate reporting

Example:

```bash
nmap 192.168.1.1 > scan_results.txt
```

---

# Key Takeaways

- `>` overwrites file contents.
- `>>` appends data to a file.
- `<` provides input from a file.
- `2>` redirects error messages.
- `|` connects multiple commands.
- `/dev/null` discards unwanted output.

---

# Interview Questions

1. What is Input/Output Redirection?
2. What is the difference between `>` and `>>`?
3. What does `2>` do?
4. What is the purpose of a pipe (`|`)?
5. What is `/dev/null` used for?

---

# Next Topic

➡️ **24-Log-Analysis.md**
