# DHCP Configuration in a Wireless LAN (Packet Tracer)

## 📌 Overview
This project demonstrates the configuration and behavior of a DHCP server within a wireless router in a Local Area Network (LAN), using Cisco Packet Tracer. The objective is to enable automatic IP address assignment and validate network connectivity between multiple client devices.

---

## 🎯 Objective
- Configure a wireless router as a DHCP server  
- Modify the router’s default IP address  
- Define a custom DHCP address range  
- Enable DHCP on client devices  
- Verify network connectivity using ping tests  

---

## 🏗️ Network Topology
- 1 Wireless Router  
- 3 PCs connected via Ethernet  
- Single LAN: 192.168.5.0/24  

---

## ⚙️ Configuration Steps

### 1. Router IP Address Change
The default router IP address was modified:


192.168.0.1 → 192.168.5.1


This change redefined the network gateway and required all clients to renew their IP configuration.

---

### 2. DHCP Configuration
The DHCP pool was configured as follows:


Starting IP Address: 192.168.5.126
Maximum Users: 75


This defines the range of IP addresses automatically assigned to clients in the network.

---

### 3. DHCP Renewal Process
All client devices were set to renew their network configuration by switching from Static to DHCP mode.

This forced the router to reassign valid IP addresses according to the updated DHCP pool.

---

## 📡 Connectivity Tests

The following commands were used to validate network functionality:

```bash
ping 192.168.5.1
ping 192.168.5.127
```

### 📊 Results

- Successful communication with the gateway (router)  
- Successful communication between client devices  
- Network properly configured and operational  

---

## 🧠 Key Concepts Learned

- LAN architecture and communication flow  
- DHCP automatic IP allocation mechanism  
- Role of default gateway in network routing  
- Importance of IP addressing consistency  
- Basic network troubleshooting using `ping`  

---

## 🔍 Technical Insight

DHCP simplifies network administration by dynamically assigning IP addresses to devices within a defined range. When the router IP changes, all clients must renew their DHCP lease to maintain connectivity within the updated subnet.

This mechanism ensures scalability, reduces manual configuration, and prevents IP conflicts in local networks.

---

## 🧭 Conclusion

This lab demonstrates the fundamental behavior of a DHCP-based LAN environment. While simple in structure, it reflects real-world networking principles and serves as a foundation for more advanced topics such as subnetting, network segmentation, and traffic analysis.
