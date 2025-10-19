# 🧠 NetworkLab Project

This project was created as part of my **CompTIA Network+** learning journey.  
It demonstrates basic network setup and configuration using **Cisco Packet Tracer**, including router, switch, server, and multiple PCs.

---

## 🎯 Project Overview

The goal of this project is to design and configure a small **Local Area Network (LAN)** that allows communication between multiple devices using **IP addressing, DNS, and DHCP** principles.

---

## 🧩 Network Topology

**Devices Used:**
- 2 × PCs (Clients)
- 1 × Switch
- 1 × Router
- 1 × Server (for DNS and DHCP services)

**Connections:**
- PCs → Switch (FastEthernet)
- Server → Switch
- Switch → Router (GigabitEthernet 0/0/0)

![Network Topology](topology_screenshot.png)

---

## ⚙️ Configuration Summary

### 🖥️ PCs
Each PC has:
- **Static IP Address:**  
  - PC1 → 192.168.1.10  
  - PC2 → 192.168.1.20
- **Subnet Mask:** 255.255.255.0
- **Default Gateway:** 192.168.1.1
- **DNS Server:** 192.168.1.100

### 🌐 Router
**Interface GigabitEthernet0/0/0**
- IP Address: 192.168.1.1
- Subnet Mask: 255.255.255.0
- `no shutdown`

### 🧠 Switch
**Management VLAN 1**
- IP Address: 192.168.1.2
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.1.1

### 💾 Server
- IP Address: 192.168.1.100
- Services:  
  - DHCP (optional)  
  - DNS (optional)
- Example DNS Record:  
  - `www.local.test -> 192.168.1.100`

---

## 🧪 Testing

Ping tests were performed to verify connectivity:

| Source  | Destination | Result             |
|---------|------------|------------------|
| PC1     | PC2        | ✅ Ping Successful |
| PC1     | Router1    | ✅ Ping Successful |
| PC1     | Server1    | ✅ Ping Successful |
| PC1     | pc2.local  | ✅ Ping Successful |
| PC2     | PC1        | ✅ Ping Successful |
| PC2     | Router1    | ✅ Ping Successful |
| PC2     | Server1    | ✅ Ping Successful |
| Server1 | PC1        | ✅ Ping Successful |
| Server1 | PC2        | ✅ Ping Successful |
| Server1 | Router1    | ✅ Ping Successful |

✅ **All connections are functional and stable.**

---

## 🛠️ Tools Used
- **Cisco Packet Tracer**
- **Windows Command Prompt (ping tests)**
- **Basic CLI configuration**

---

## 📁 Project Files
- `NetworkLab.pkt` → Cisco Packet Tracer topology file  
- `README.md` → Project documentation  
- `configurations.txt` → All CLI commands used  
- `topology_screenshot.png` → Network diagram  

---

## 👩🏻‍💻 Author
**Atussa**  
💻 IT Enthusiast | Network & Cybersecurity Learner  
📍 Based in Iran  
🔗 [GitHub](https://github.com/odarkpxlo)
