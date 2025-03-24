# Subnetting Guide

## ✅ What is Subnetting?

**Subnetting** is the process of dividing a larger network into smaller, more manageable sub-networks or "subnets." It improves network performance and security by isolating network traffic and reducing broadcast domains.

Subnetting allows network administrators to efficiently allocate IP addresses and reduce IP waste.

---

## ✅ Subnetting Calculation Examples

### Example 1: IP Address `192.168.10.0/24`
- **Subnet Mask:** 255.255.255.0
- **Total IPs:** 256
- **Usable Hosts:** 254 (minus network & broadcast address)
- **Subnets Possible (if split into /26):** 4 subnets

### Example 2: Subnet `192.168.10.0/26`
- **Subnet Mask:** 255.255.255.192
- **Block Size:** 64 IPs per subnet
- **Usable Hosts:** 62 per subnet

| Subnet | Network Address | First Host | Last Host | Broadcast Address |
|--------|------------------|------------|-----------|-------------------|
| 1      | 192.168.10.0     | .1         | .62       | 192.168.10.63     |
| 2      | 192.168.10.64    | .65        | .126      | 192.168.10.127    |

---

## ✅ Screenshot (IP Configuration Example)
> *(Replace this with your own screenshot or upload one to your GitHub repo and embed it here)*

```
Windows Static IP Configuration:
- IP Address: 192.168.1.100
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.1.1
```

```
Linux Static IP Configuration:
sudo nmcli connection modify 'Wired connection 1' ipv4.addresses 192.168.1.100/24
sudo nmcli connection modify 'Wired connection 1' ipv4.gateway 192.168.1.1
sudo nmcli connection modify 'Wired connection 1' ipv4.method manual
sudo nmcli connection up 'Wired connection 1'
```

---

## ✅ Tools & Resources Used
- [Subnetting Practice Tool](https://subnettingpractice.com/)
- [SolarWinds IP Subnet Calculator](https://www.solarwinds.com/free-tools/ip-subnet-calculator)
- [Subnetting in Computer Networks - GeeksForGeeks](https://www.geeksforgeeks.org/subnetting-in-computer-network/)
- YouTube: Networking & Subnetting Videos

---

## ✅ Reflection
Subnetting can be tricky at first, but with practice it becomes easier. It’s crucial for designing efficient networks and ensuring IP address conservation. Understanding how to split and assign IP blocks is key to being an effective IT Support or Network Technician.
