# 🏨 Smart Hotel Network Simulation

**Course:** Computer Networks Lab (CSC319 – Fall 2025)  
**Instructor:** Taha Shaikh  

---

## 📌 Project Overview

The **Smart Hotel Network Simulation** is a computer networks lab project that demonstrates the design and implementation of a secure, scalable, and well-segmented hotel network using enterprise networking concepts.

The network supports multiple hotel departments such as **Reception, Guests, Staff, Security, and Servers**, each isolated using VLANs while allowing controlled communication through routing and security mechanisms.

This project was implemented and tested in a simulated environment using Cisco Packet Tracer.

---

## 🎯 Objectives

### Functional Objectives
- Design a multi-VLAN hotel network
- Enable inter-VLAN routing using Router-on-a-Stick
- Implement Dynamic IP allocation (DHCP)
- Configure Multi-Area OSPF routing
- Provide internet connectivity to authorized users
- Validate network functionality through testing

### Security Objectives
- Isolate departments using VLANs
- Restrict guest access to internal hotel resources
- Implement Access Control Lists (ACLs)
- Enable secure external access using NAT Overload (PAT)
- Protect private IP addressing

---

## 🧱 Network Design

### VLAN Segmentation

| VLAN ID | Department | Subnet |
|------|-----------|--------|
| 10 | Reception | 192.168.10.0/28 |
| 20 | Guests | 192.168.20.0/26 |
| 30 | Staff | 192.168.30.0/27 |
| 40 | Security | 192.168.40.0/28 |
| 50 | Servers | 192.168.50.0/28 |

---

### Technologies Used
- VLANs and Trunking (802.1Q)
- Router-on-a-Stick Inter-VLAN Routing
- DHCP for dynamic IP allocation
- Multi-Area OSPF Routing
- Floating Static Routes (Backup)
- Access Control Lists (ACLs)
- NAT Overload (PAT)
- DNS for static devices

---

## 🔐 Security Implementation

- Guest VLAN (VLAN 20) is restricted from accessing:
  - Staff VLAN
  - Security VLAN
  - Server VLAN
- Guests are allowed internet access via NAT
- Extended ACL applied inbound on Guest VLAN sub-interface
- Standard ACL used for NAT control
- DNS configured for:
  - Hotel Server
  - Staff Printer
  - ISP Server

---

## 🧪 Testing & Results

- Intra-VLAN and Inter-VLAN connectivity verified
- DHCP assignment validated across all VLANs
- Guest access restrictions successfully enforced
- NAT translations confirmed
- DNS hostname resolution tested

---

## ⚠️ Limitations

- Single-router VLAN simulation
- Simplified ISP network
- Limited wireless security
- No hardware redundancy or failover testing
- Advanced firewall features not implemented

---

## 🚀 Future Improvements

- WPA2/WPA3-Enterprise wireless security
- Dedicated firewall implementation
- Redundant routers and switches
- Load balancing
- Network monitoring and logging

---

## 👥 Team Members

- Areej Mazhar (20231-34638)
- Muneeba Shoukat (20231-35056)
- Rafay Khan (20231-34594)
- Somil (20231-34062)

---

## 🛠 Tools Used

- Cisco Packet Tracer
- Cisco IOS (Routing & Switching)

---

## 📄 License

This project is developed for **academic and educational purposes only**.
