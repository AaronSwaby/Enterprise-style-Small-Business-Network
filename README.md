# 📡 Small Business Enterprise Network – Cisco Packet Tracer

This project simulates a small-to-medium business enterprise network using Cisco Packet Tracer, implementing realistic industry practices such as VLAN-based segmentation, Layer 3 switching, dynamic routing, VoIP integration, and secure internet access using NAT.

---

## 📌 Project Overview

The network is designed to support multiple departments, centralized services, voice communications, and external connectivity while maintaining security, scalability, and performance. It reflects a hierarchical enterprise-style architecture commonly used in real-world environments.

---

## 🧱 Core Architecture

### Layer 3 Core Switch (CEN_SW)
- Inter-VLAN routing enabled  
- Default gateway for all internal VLANs  
- DHCP relay using `ip helper-address`  
- EIGRP routing (AS 100)  

### Access Layer Switches
- Department-based VLAN access  
- Trunked uplinks to the core switch  

---

## 🏢 VLAN & Subnet Design

| VLAN | Department        | Subnet           |
|------|-----------------|----------------|
| 10   | Coding Staff     | 192.168.0.192/27 |
| 20   | HR               | 192.168.0.224/27 |
| 30   | Front Desk       | 192.168.0.128/26 |
| 40   | Customer Service | 192.168.0.0/25   |
| 50   | Server / IT      | 172.16.0.0/24    |
| 60   | Infrastructure   | 192.168.1.16/28  |
| 70   | Voice            | 192.168.1.0/28   |
| 80   | Guest / Expansion| 192.168.1.32/28  |

---

## 📞 VoIP Implementation
- Cisco Call Manager Express (CME) configured  
- DHCP Option 150 for IP phone TFTP  
- Cisco 7960 IP Phones  
- Extensions 101–110  
- Voice traffic isolated in VLAN 70  

---

## 🌐 Routing & Internet Connectivity
- EIGRP (AS 100) between core switch and routers  
- Default route toward ISP  
- NAT overload (PAT) using public IP pool  
- WAN simulation using public IP addressing  

---

## 🔐 Security & Network Services
- Access Control Lists (ACLs) to restrict server access  
- DHCP relay via `ip helper-address`  
- Centralized NTP and Syslog server  
- Inside / Outside NAT separation  

---

## 📁 Repository Contents
- `Small_Business_Network.pkt` – Cisco Packet Tracer topology
- `Small_Business_Network.png` – Topology Overview 
- `README.md` – Project documentation  

---

## 🎯 Network Features & Capabilities
- VLAN design & VLSM subnetting  
- Layer 3 switching  
- Dynamic routing (EIGRP)  
- VoIP (CME & IP Phones)  
- NAT & WAN connectivity  
- ACL-based traffic control  

---

## 👤 Author
*Aaron Swaby* 

Cisco Packet Tracer Enterprise Network Project
