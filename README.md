# 🏨 Smart Hotel Network Simulation
[cite_start]**Institution:** Institute of Business Management   
[cite_start]**Course:** Computer Networks Lab (Fall 2025) [cite: 1, 2]

## Project Overview
[cite_start]This project simulates a secure, enterprise-grade network for a smart hotel[cite: 60]. [cite_start]It features departmental segmentation, dynamic routing to an ISP, and strict security policies[cite: 61, 63, 65].

## 🚀 Key Technical Features
* [cite_start]**Multi-Area OSPF:** Dynamic routing between the Hotel (Area 1), Backbone (Area 0), and ISP (Area 2)[cite: 200, 201, 203, 204].
* [cite_start]**Network Security:** * **Extended ACLs:** Blocks Guest VLAN access to sensitive Staff, Security, and Server subnets[cite: 234, 236].
    * [cite_start]**NAT/PAT:** Configured on the Hotel_Router to allow internal private IPs to reach the internet[cite: 247, 248].
* [cite_start]**VLAN Segmentation:** Isolated broadcast domains for Reception, Guests, Staff, Security, and Servers[cite: 104, 137].
* [cite_start]**Redundancy:** Floating static routes (AD 120) serve as a backup to OSPF[cite: 208, 209].

## 📊 Addressing Scheme
| VLAN | Department | Subnet | Gateway |
| :--- | :--- | :--- | :--- |
| 10 | Reception | 192.168.10.0/28 | 192.168.10.1 |
| 20 | Guests | 192.168.20.0/26 | 192.168.20.1 |
| 50 | Servers | 192.168.50.0/28 | 192.168.50.1 |

[cite_start][cite: 137, 142]

## 🧪 Verified Testing
* [cite_start]**Inter-VLAN Connectivity:** Verified pings between Staff_PC1 and Hotel_Server[cite: 285].
* [cite_start]**External Access:** Verified Guest devices accessing the ISP_Server via NAT[cite: 288].
* [cite_start]**ACL Enforcement:** Verified "Destination host unreachable" when Guests attempt to ping Staff VLAN[cite: 291, 292].
