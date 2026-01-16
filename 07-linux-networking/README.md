
# Linux Networking

This section covers **network configuration and monitoring** in Linux, including interface management, connectivity testing, and troubleshooting commands.

---

## Introduction to Linux Networking

Networking in Linux involves managing interfaces, routing, IP addresses, and connectivity. Proper network monitoring and configuration are crucial for system communication and troubleshooting.

---

## Network Interface Management

### Display all network interfaces

```bash
ip a
```

> Shows all network interfaces with IP addresses and status.

### Bring an interface up or down

```bash
ip link set eth0 up
```

```bash
ip link set eth0 down
```

> Replace `eth0` with your interface name.

### Check interface configuration (legacy)

```bash
ifconfig
```

> Deprecated in favor of `ip a`.

---

## IP Address Management

### Assign a static IP

```bash
sudo ip addr add 192.168.1.10/24 dev eth0
```

### Remove an IP

```bash
sudo ip addr del 192.168.1.10/24 dev eth0
```

### Set default gateway

```bash
sudo ip route add default via 192.168.1.1
```

### View routing table

```bash
ip route
```

---

## Testing Connectivity

### Ping a host

```bash
ping google.com
```

> Tests network connectivity to a host.

### Trace network path

```bash
traceroute google.com
```

> Shows the route packets take to reach the host.

### DNS resolution

```bash
nslookup example.com
```

> Checks DNS resolution for a domain.

---

## Viewing Open Ports and Connections

### Using `netstat`

```bash
netstat -tulnp
```

### Using `ss`

```bash
ss -tulnp
```

> `ss` is a modern alternative to `netstat`.

---

## Network Diagnostics

### Test network interface with `ethtool`

```bash
sudo ethtool eth0
```

> Displays interface speed, duplex, and link status.

### Check network statistics

```bash
ifconfig eth0
```

```bash
ip -s link
```

---

## Advanced Network Monitoring

### Monitor traffic in real-time with `tcpdump`

```bash
sudo tcpdump -i eth0
```

### Check bandwidth usage with `nload` (requires installation)

```bash
nload eth0
```
