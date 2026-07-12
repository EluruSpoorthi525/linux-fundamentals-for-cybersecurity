# Shell Scripting Basics

## Introduction

A **shell script** is a text file containing a series of Linux commands that are executed automatically by the shell. Shell scripting helps automate repetitive tasks, improve productivity, and simplify system administration.

Shell scripts are widely used by Linux administrators, DevOps engineers, and cybersecurity professionals for automation.

---

# Why Use Shell Scripts?

Shell scripts help to:

- Automate repetitive tasks
- Save time
- Reduce human errors
- Manage Linux systems efficiently
- Perform scheduled tasks

---

# Creating a Shell Script

Create a script file:

```bash
touch script.sh
```

Give execute permission:

```bash
chmod +x script.sh
```

Run the script:

```bash
./script.sh
```

---

# Shebang (#!)

Every shell script should begin with a **shebang**, which tells Linux which interpreter to use.

Example:

```bash
#!/bin/bash
```

---

# Your First Script

```bash
#!/bin/bash

echo "Hello, Linux!"
```

Run it:

```bash
./script.sh
```

Output:

```text
Hello, Linux!
```

---

# Variables

Create a variable:

```bash
name="Spoorthi"
```

Display a variable:

```bash
echo $name
```

---

# User Input

Read input from the user:

```bash
#!/bin/bash

echo "Enter your name:"
read name

echo "Welcome, $name"
```

---

# Comments

Single-line comment:

```bash
# This is a comment
```

Comments improve code readability.

---

# Basic Operators

Arithmetic:

```bash
a=10
b=5

echo $((a+b))
echo $((a-b))
echo $((a*b))
echo $((a/b))
```

---

# Best Practices

- Use meaningful variable names.
- Add comments where necessary.
- Keep scripts simple and organized.
- Test scripts before using them in production.
- Give execute permission only when needed.

---

# Cybersecurity Relevance

Shell scripting is widely used to:

- Automate security checks
- Analyze log files
- Create backup scripts
- Scan systems
- Automate incident response tasks

---

# Key Takeaways

- Shell scripts automate Linux tasks.
- Every script starts with `#!/bin/bash`.
- `chmod +x` makes a script executable.
- Variables store data.
- `read` accepts user input.

---

# Interview Questions

1. What is a shell script?
2. What is the purpose of the shebang (`#!/bin/bash`)?
3. How do you execute a shell script?
4. How do you create a variable in Bash?
5. Why is shell scripting important?

---

# Next Topic

➡️ **21-Bash-Scripting.md**
```
