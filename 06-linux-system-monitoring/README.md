
# Linux System Monitoring

This section covers **system monitoring** in Linux, including CPU, memory, disk, network, and log monitoring with practical commands.

---

## Introduction to System Monitoring

Monitoring system resources is essential to ensure optimal performance, detect issues, and troubleshoot problems in Linux. Various tools allow us to monitor CPU, memory, disk usage, network activity, and running processes.

---

## CPU and Memory Monitoring

### Using `top` (Real-time system monitoring)

```bash
top
```

> Press `q` to quit.

### Using `htop` (Interactive process viewer)

```bash
htop
```

> Use arrow keys to navigate and `F9` to kill processes. Requires installation.

### Using `vmstat`

```bash
vmstat 1 5
```

> Updates every 1 second, showing 5 updates of CPU, memory, and I/O statistics.

### Checking Memory Usage

```bash
free -m
```

> Displays free and used memory in megabytes.

---

## Disk Monitoring

### Using `df` (Disk free space)

```bash
df -h
```

> Shows available disk space in human-readable format.

### Using `du` (Disk usage of directories)

```bash
du -sh /var/log
```

> Shows size of a specific directory.

### Using `iostat` (CPU and disk I/O statistics)

```bash
iostat
```

---

## Network Monitoring

### Checking Network Interfaces

```bash
ip a
```

> Shows IP addresses and interface details.

### Viewing Open Ports and Connections

```bash
netstat -tulnp
```

```bash
ss -tulnp
```

> `ss` is a modern alternative to `netstat`.

### Testing Connectivity

```bash
ping google.com
```

```bash
traceroute google.com
```

### Checking DNS Resolution

```bash
nslookup example.com
```

---

## Log Monitoring

### Live Monitoring of System Logs

```bash
tail -f /var/log/syslog
```

```bash
journalctl -f
```

> `journalctl` works for systemd-based distributions.

### Checking Kernel Logs

```bash
dmesg | tail
```
````
