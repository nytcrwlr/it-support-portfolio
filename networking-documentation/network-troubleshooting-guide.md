# Network Troubleshooting Guide

## ✅ Common Network Tools (Windows & Linux)

| Tool      | Platform(s)        | Purpose                                   |
|-----------|--------------------|-------------------------------------------|
| `ping`    | Windows/Linux       | Test connectivity between two hosts       |
| `ipconfig`| Windows             | View IP configuration details             |
| `ifconfig`/`ip`| Linux          | View and configure network interfaces     |
| `tracert` | Windows             | Trace route to destination (hops)         |
| `traceroute` | Linux            | Same as tracert (UNIX/Linux equivalent)   |
| `nslookup`| Windows/Linux       | Query DNS servers                         |
| `netstat` | Windows/Linux       | Show active network connections & ports   |
| `nmap`    | Windows/Linux       | Network scanner for host/port discovery   |

---

## ✅ When to Use Each Tool

- **`ping`** – Check if a host is reachable and responding
- **`ipconfig` / `ifconfig` / `ip`** – Diagnose IP conflicts or missing IP addresses
- **`tracert` / `traceroute`** – Identify where packet loss or delays occur in a route
- **`nslookup`** – Diagnose DNS issues
- **`netstat`** – Detect unwanted or suspicious open connections/ports
- **`nmap`** – Scan a device or network to identify open ports/services

---

## ✅ Example Outputs

### `ping google.com`
```
Reply from 142.250.64.78: bytes=32 time=14ms TTL=117
```

### `ipconfig` (Windows)
```
Ethernet adapter Ethernet:
   IPv4 Address. . . . . . . . . . . : 192.168.1.101
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : 192.168.1.1
```

### `tracert google.com`
```
1   <1 ms   <1 ms   <1 ms  192.168.1.1
2     8 ms     9 ms    10 ms  10.10.0.1
3    20 ms    19 ms    20 ms  142.250.64.78
```

### `nslookup google.com`
```
Server:  dns.google
Address:  8.8.8.8

Non-authoritative answer:
Name:    google.com
Addresses:  142.250.64.78
```

---

## ✅ Notes & Observations
- When troubleshooting no internet access, `ping` and `ipconfig` are your first go-to tools.
- Use `tracert` or `traceroute` to spot where traffic is getting blocked or delayed.
- DNS issues can often be identified quickly with `nslookup`.
- `netstat` is useful for finding unauthorized or unexpected connections.
- `nmap` is powerful for auditing networks, but should be used responsibly.

---

**Commit message:** `"Added Network Troubleshooting Guide"`
