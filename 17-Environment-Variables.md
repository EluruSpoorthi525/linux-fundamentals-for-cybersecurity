# Environment Variables

## Introduction

Environment variables are **key-value pairs** used by the operating system and applications to store configuration settings. They help programs access important information such as system paths, usernames, home directories, and application configurations.

Environment variables make Linux systems more flexible and easier to configure without modifying program code.

---

# Why are Environment Variables Important?

Environment variables are used to:

- Store system configuration
- Locate executable programs
- Manage user-specific settings
- Configure applications
- Avoid hardcoding values

---

# Viewing Environment Variables

Display all environment variables:

```bash
printenv
```

or

```bash
env
```

Display a specific variable:

```bash
echo $HOME
```

---

# Common Environment Variables

| Variable | Description |
|----------|-------------|
| `$HOME` | User's home directory |
| `$USER` | Current username |
| `$PATH` | Directories searched for commands |
| `$PWD` | Present working directory |
| `$SHELL` | Current shell |
| `$HOSTNAME` | System hostname |

---

# PATH Variable

The **PATH** variable tells Linux where to search for executable programs.

View PATH:

```bash
echo $PATH
```

Example output:

```text
/usr/local/bin:/usr/bin:/bin
```

---

# Creating an Environment Variable

Temporary variable:

```bash
export NAME="John"
```

Verify:

```bash
echo $NAME
```

---

# Removing an Environment Variable

```bash
unset NAME
```

---

# Permanent Environment Variables

To make variables permanent, add them to:

- `~/.bashrc`
- `~/.profile`
- `~/.zshrc` (for Zsh users)

Example:

```bash
export JAVA_HOME=/usr/lib/jvm/java-17
```

Apply changes:

```bash
source ~/.bashrc
```

---

# Best Practices

- Use meaningful variable names.
- Store reusable configuration values.
- Avoid storing sensitive information in plain text.
- Verify changes after editing configuration files.

---

# Cybersecurity Relevance

Environment variables are important because they:

- Store application configurations
- Control execution paths
- Help configure development environments
- Can expose sensitive information if misconfigured

Always verify environment variables before running critical applications or scripts.

---

# Key Takeaways

- Environment variables store system and application settings.
- `printenv` and `env` display variables.
- `export` creates variables.
- `unset` removes variables.
- `$PATH` determines where Linux searches for commands.

---

# Interview Questions

1. What is an environment variable?
2. What is the purpose of the PATH variable?
3. How do you display all environment variables?
4. How do you create a temporary environment variable?
5. How do you make an environment variable permanent?

---

# Next Topic

➡️ **18-File-Compression-and-Archiving.md**
```
