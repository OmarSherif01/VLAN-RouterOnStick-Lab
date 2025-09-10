# VLAN & Router-on-a-Stick Lab (Network+ Project)

## 📌 Project Overview
This lab simulates a **small enterprise network** with multiple departments segmented using VLANs.  
The main objectives were:
- Configure **VLANs** for Admin, Sales, and IT.
- Implement **Router-on-a-Stick** for inter-VLAN routing.
- Set up **DHCP services** on the router for dynamic IP allocation.
- Apply a **basic ACL** to restrict Sales from accessing Admin while allowing other traffic.

This project was built in **Cisco Packet Tracer** as part of my hands-on practice for the CompTIA **Network+ certification** and job readiness in networking/SOC environments.

---

## 🖼️ Network Topology
![Network Topology](Network_topology.png)  
*(Two switches, one router, and six PCs across three VLANs)*

---

## 🗂️ IP Addressing Plan

| VLAN   | Network        | Subnet Mask     | Default Gateway | Department |
|--------|----------------|-----------------|----------------|------------|
| VLAN10 | 192.168.10.0   | 255.255.255.0   | 192.168.10.1   | Admin      |
| VLAN20 | 192.168.20.0   | 255.255.255.0   | 192.168.20.1   | Sales      |
| VLAN30 | 192.168.30.0   | 255.255.255.0   | 192.168.30.1   | IT         |

---

## ⚙️ Key Configurations

### VLANs on Switch
```bash
Switch(config)# vlan 10
Switch(config-vlan)# name Admin
Switch(config)# vlan 20
Switch(config-vlan)# name Sales
Switch(config)# vlan 30
Switch(config-vlan)# name IT
