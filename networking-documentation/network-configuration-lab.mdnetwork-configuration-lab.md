# Network Device Configuration Lab (Cisco Packet Tracer)

## ✅ Device Layout and IP Assignments
| Device | Interface       | IP Address     | Subnet Mask       |
|--------|------------------|----------------|-------------------|
| PC0    | FastEthernet0    | 192.168.1.10   | 255.255.255.0     |
| PC1    | FastEthernet0    | 192.168.1.20   | 255.255.255.0     |
| Switch0| N/A              | N/A            | N/A               |
| Router0| FastEthernet0/0  | 192.168.1.1    | 255.255.255.0     |

---

## ✅ Configuration Commands Used
### Router Configuration:
```bash
Router> enable
Router# configure terminal
Router(config)# interface fastEthernet 0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown
Router(config-if)# exit
Router(config)# exit
Router# write memory
```

### PC IP Configuration:
- On both PCs:
  - Open Desktop > IP Configuration
  - Enter the assigned IP address and subnet mask
  - Set Default Gateway to 192.168.1.1

---

## ✅ Ping Test Results
### From PC0 to PC1:
```
> ping 192.168.1.20
Reply from 192.168.1.20: bytes=32 time<1ms TTL=128
```

### From PC0 to Router:
```
> ping 192.168.1.1
Reply from 192.168.1.1: bytes=32 time<1ms TTL=255
```

✅ Both ping tests were successful, indicating proper configuration and connectivity between devices.

---

## ✅ Screenshot (Optional)
> *(Insert screenshot of Packet Tracer layout here. You can upload it to your GitHub repo and link it)*

---

## ✅ Notes
This simple LAN setup using Cisco Packet Tracer demonstrates basic network configuration, including setting static IPs and router interface settings. The success of ping tests confirms that the network is correctly configured for communication between hosts.

---

