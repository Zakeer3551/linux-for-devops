
# Linux Process Management

This section covers **process management** in Linux, including viewing, controlling, and monitoring processes.

---

## Introduction to Process Management

A process is an instance of a running program. Linux provides multiple utilities to monitor, manage, and control processes effectively. Each process has a unique **Process ID (PID)** and belongs to a parent process.

---

## Viewing Processes

### View all running processes

```bash
ps aux
```

### View processes for a specific user

```bash
ps -u username
```

### Show a process by name

```bash
ps -C processname
```

### Find a process by name and return its PID

```bash
pgrep processname
```

### Find the PID of a running program

```bash
pidof processname
```

---

## Managing Processes

### Terminate a process by PID

```bash
kill PID
```

### Terminate a process by name

```bash
pkill processname
```

### Force kill a process

```bash
kill -9 PID
```

### Kill all instances of a process

```bash
pkill -9 processname
```

### Stop a running process

```bash
kill -STOP PID
```

### Resume a stopped process

```bash
kill -CONT PID
```

### Change process priority

Lower priority:

```bash
renice -n 10 -p PID
```

Increase priority (requires root):

```bash
renice -n -5 -p PID
```

---

## Background & Foreground Processes

### Run a command in the background

```bash
command &
```

### List background jobs

```bash
jobs
```

### Bring a job to the foreground

```bash
fg %jobnumber
```

### Suspend a running process

```text
Ctrl + Z
```

### Resume a suspended process in the background

```bash
bg %jobnumber
```

---

## Monitoring System Processes

### Using `top` (interactive process viewer)

```bash
top
```

> Press `k` and enter a PID to kill a process  
> Press `r` to renice a process  
> Press `q` to quit

### Using `htop` (user-friendly alternative)

```bash
htop
```

> Allows mouse-based interaction for process management (requires installation)

### Using `nice` to run a command with a specific priority

```bash
nice -n 10 command
```

### Using `renice` to change priority of an existing process

```bash
renice -n -5 -p PID
```

---

## Daemon Processes

Daemon processes run in the background without user intervention.

### List all system daemons

```bash
systemctl list-units --type=service
```

### Start a daemon/service

```bash
systemctl start service-name
```

### Stop a daemon/service

```bash
systemctl stop service-name
```

### Enable a service at startup

```bash
systemctl enable service-name
```
````
