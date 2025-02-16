# 🌊 Underwater Research Station Project 📡

## 📄 Project Overview
The Underwater Research Station project simulates a robust network infrastructure to support scientific research and real-time monitoring beneath the ocean. This document provides a complete setup guide, IP configuration table, and key highlights.

---

## 🗺️ Network Diagram Summary
The network is divided into two primary sections:

### 1️⃣ Land Station Base
- Workstations
- Command Center
- Servers
- VPN Access for Remote Users

### 2️⃣ Underwater Research Base
- Research Workstations
- Command Center
- Sensors, Detectors, and Monitors
- Surveillance Cameras
- Robots and Controllers

---

## 📡 Network Devices & Connectivity
| **Device Name**         | **Device Type** | **IP Address**      | **Notes**                          |
|-------------------------|-----------------|---------------------|--------------------------------------|
| Land Base Router 1      | Router         | 90.0.0.1 / 80.0.0.1 | Connects Land Base & Underwater Base|
| Land Base Switch        | Switch         | N/A                 | Core Switch at Land Station         |
| ASA Firewall            | Firewall       | 192.168.1.1 (Inside) / 192.168.2.1 (Outside) | Securing Database Access |
| Database 1 Server       | Server         | 90.0.0.11 / 192.168.1.10 | Database Server 1                  |
| Database 2 Server       | Server         | 90.0.0.12 / 192.168.1.20 | Database Server 2                  |
| Workstations WS-02 to WS-07 | PCs        | 90.0.0.X            | Land Station Workstations           |
| Command Center CC-08 to CC-10 | PCs     | 90.0.0.X            | Land Command Center PCs             |
| Remote Users PC/Laptop  | PCs/Laptops    | 192.168.2.X         | VPN-connected Users                 |
| Sea Router              | Router         | 30.0.0.1 / 80.0.0.2 | Connects Underwater & Land Base     |
| Underwater Router 2     | Router         | 60.0.0.1 / 70.0.0.1 | Connects Underwater Units           |
| Underwater Command Switch | Switch       | N/A                 | Central Underwater Switch           |
| Research Workstations   | PCs            | 10.0.0.X            | Underwater Research PCs             |
| Underwater Command Center PCs | PCs     | 20.0.0.X            | Underwater Command PCs              |
| Sensors/Monitors        | Devices        | 50.0.0.X            | Environmental Monitoring Sensors    |
| Surveillance Cameras    | Cameras        | 40.0.0.X            | Underwater Surveillance Cameras     |
| Robots & Controllers    | Devices        | 70.0.0.X            | Underwater Robotics Controllers     |

---

## 🔐 Security & VPN Configuration
- **SSL VPN** provides secure remote access for users outside the base.
- **ASA Firewall** segments database servers into VLANs for secure communication.
- **IP Address Segmentation** ensures isolation between land, underwater, and external users.

---

## ⚙️ Key Functionalities
✅ Real-time Data Monitoring 🖥️
✅ Remote Access via SSL VPN 🌐
✅ Underwater Surveillance 🎥
✅ Environmental Sensors (Temp, Humidity, Gas, Sound) 🌡️
✅ Robotics Control 🤖
✅ Secure Data Management 🔒

---

## 📝 Final Summary
This network design supports high-level underwater research with secure communication and real-time data transfer between land and underwater bases. It combines surveillance, environmental monitoring, and remote access for complete operational efficiency.

---

## 🚀 Get Started
1. Deploy Cisco Packet Tracer simulation.
2. Configure routers, switches, servers, and firewalls as per the IP address table.
3. Test VPN connectivity and sensor data transmission.

🛠️ Built using **Cisco Packet Tracer**
📤 Upload your simulation to **GitHub** and share it with the community!

📧 For inquiries, contact: **nivassai2506@gmail.com**

