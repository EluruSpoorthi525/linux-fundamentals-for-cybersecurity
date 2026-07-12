# Process Management

## Introduction

A **process** is an instance of a running program. Whenever you open an application, execute a command, or start a service, Linux creates one or more processes to perform the requested task.

Linux is a multitasking operating system, allowing multiple processes to run simultaneously. The Linux kernel manages these processes by allocating CPU time, memory, and other system resources.

Understanding process management is essential for system administrators and cybersecurity professionals because it helps monitor system activity, troubleshoot issues, identify malicious programs, and optimize performance.

---

# What is a Process?

A process is a program that is currently executing.

Examples:

* Opening Firefox creates a process.
* Running the `ls` command creates a process.
* Starting an SSH server creates one or more processes.

Each process has:

* Process ID (PID)
* Parent Process ID (PPID)
* Owner
* Priority
* Memory usage
* CPU usage
* Process state

---

# Process Lifecycle

A process goes through several states during execution.

```text
New
 │
 ▼
Ready
 │
 ▼
Running
 │
 ├────────► Waiting
 │              │
 ▼              │
Terminated ◄────┘
```

---

# Process States

| State        | Description                                 |
| ------------ | ------------------------------------------- |
| Running (R)  | Currently executing on the CPU              |
| Sleeping (S) | Waiting for an event or resource            |
| Stopped (T)  | Suspended by the user or system             |
| Zombie (Z)   | Finished execution but awaiting cleanup     |
| Idle (I)     | Waiting for CPU scheduling (kernel threads) |

---

# Viewing Running Processes

## ps

Displays information about active processes.

Basic usage:

```bash
ps
```

Display all running processes:

```bash
ps -e
```

Detailed information:

```bash
ps -ef
```

BSD-style format:

```bash
ps aux
```

Example output:

```text
USER       PID %CPU %MEM COMMAND
student   1542  0.2  1.5 bash
student   1824  3.1  4.8 firefox
```

---

# Monitoring Processes

## top

Displays real-time system and process information.

```bash
top
```

Information shown:

* CPU usage
* Memory usage
* Running processes
* Process IDs
* Load average

Press **q** to quit.

---

## htop

An enhanced version of `top` with an interactive interface.

```bash
htop
```

Features:

* Colored output
* Easy navigation
* Process search
* Interactive process management

> Note: `htop` may need to be installed separately.

---

# Finding a Process

Use `pgrep` to search for a process by name.

```bash
pgrep firefox
```

List matching processes with names:

```bash
pgrep -l ssh
```

---

# Viewing Process Tree

Display parent-child relationships:

```bash
pstree
```

Example:

```text
systemd
 ├── NetworkManager
 ├── sshd
 ├── gnome-shell
 └── firefox
```

---

# Killing Processes

## kill

Terminates a process using its PID.

```bash
kill 1542
```

Force terminate:

```bash
kill -9 1542
```

> **Warning:** `kill -9` immediately terminates a process without allowing it to clean up resources.

---

## pkill

Kill processes by name.

```bash
pkill firefox
```

---

## killall

Terminate all processes with the same name.

```bash
killall firefox
```

---

# Background Processes

Run a command in the background:

```bash
firefox &
```

View background jobs:

```bash
jobs
```

Bring a job to the foreground:

```bash
fg %1
```

Resume a stopped job in the background:

```bash
bg %1
```

---

# Process Priority

Linux assigns each process a scheduling priority.

## nice

Start a process with a specific priority:

```bash
nice -n 10 command
```

Higher nice values = lower priority.

---

## renice

Change the priority of a running process.

```bash
sudo renice 5 -p 1542
```

---

# Signals

Signals allow processes to communicate.

Common signals:

| Signal  | Number | Purpose                        |
| ------- | ------ | ------------------------------ |
| SIGTERM | 15     | Gracefully terminate a process |
| SIGKILL | 9      | Forcefully terminate a process |
| SIGSTOP | 19     | Pause a process                |
| SIGCONT | 18     | Resume a paused process        |

Example:

```bash
kill -15 1542
```

---

# Process Management Workflow

```text
Start Process
      │
      ▼
Monitor Process
      │
      ▼
Adjust Priority
      │
      ▼
Terminate Process
```

---

# Best Practices

* Monitor CPU and memory usage regularly.
* Use `kill -9` only when a process does not respond to `SIGTERM`.
* Avoid terminating critical system processes.
* Use `top` or `htop` to identify resource-intensive processes.
* Investigate unexpected or unknown processes.

---

# Cybersecurity Relevance

Process management is vital in cybersecurity because professionals often need to:

* Detect malicious processes
* Stop malware
* Monitor system activity
* Investigate unauthorized applications
* Analyze resource usage
* Respond to security incidents

Example:

Find SSH processes:

```bash
pgrep -l ssh
```

Terminate a suspicious process:

```bash
kill PID
```

Monitor processes in real time:

```bash
top
```

---

# Key Takeaways

* A process is a running instance of a program.
* Every process has a unique Process ID (PID).
* `ps` displays running processes.
* `top` and `htop` monitor processes in real time.
* `kill`, `pkill`, and `killall` terminate processes.
* `nice` and `renice` control process priority.
* Understanding process management is essential for Linux administration and cybersecurity.

---

# Interview Questions

1. What is a process in Linux?
2. What is a PID?
3. What is the difference between `ps` and `top`?
4. What does `kill -9` do?
5. What is the purpose of `pkill`?
6. What is a zombie process?
7. What does the `nice` command do?
8. What is the difference between foreground and background processes?
9. What are Linux signals?
10. Why is process management important in cybersecurity?

---

# Hands-on Practice

Run the following commands on your Linux system:

```bash
ps
ps -ef
ps aux

top

sleep 300 &
jobs

pgrep sleep

kill $(pgrep sleep)

nice -n 10 sleep 100 &
jobs
```

Observe how processes are created, monitored, prioritized, and terminated.

---

# Next Topic

➡️ **15-Package-Management.md** – Learn how to install, update, remove, and manage software packages using package managers such as **APT**, **DNF**, **YUM**, and **Pacman** across different Linux distributions.

