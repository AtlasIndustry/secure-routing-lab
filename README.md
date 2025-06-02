# Secure Enterprise Network Lab

This Packet Tracer project simulates a segmented enterprise network designed for secure inter-VLAN routing, access control, and multi-protocol routing. It reflects realistic infrastructure environments where routing security, VLAN separation, and traffic restrictions are critical.

![image](https://github.com/user-attachments/assets/05c2b26e-69c4-45d7-af16-244aa3f719a0)


---

## Objective

Build a scalable, security-focused lab demonstrating:
- Logical VLAN segmentation (HR and Engineering)
- Inter-VLAN routing via router subinterfaces
- OSPF and EIGRP deployment with route redistribution
- Access Control Lists (ACLs) to enforce internal access restrictions

---

## Topology Overview

| Device    | IP Address        | Role / VLAN       |
|-----------|------------------|-------------------|
| PC1       | 192.168.10.10     | HR (VLAN 10)      |
| PC2       | 192.168.20.10     | Engineering (VLAN 20) |
| PC3       | 192.168.30.10     | Engineering (VLAN 30) |
| PC4       | 192.168.40.10     | Engineering (VLAN 40) |
| Server0   | 192.168.99.10     | Restricted Internal Server (VLAN 99) |
| Router0   | Core router (Route redistribution + ACLs) |
| Router1   | HR site router (OSPF) |
| Router2   | Engineering site router (EIGRP) |
| Switches  | L2 VLAN control and trunking |

---

## Security Features

- ACL blocks Engineering VLANs from accessing Server0
- HR VLAN (PC1) is the only host allowed server access
- Inter-VLAN isolation enforced with subinterfaces and ACLs
- Trunk links simulate enterprise switch-to-router environments

---

## Technologies Used

- Cisco Packet Tracer
- VLANs (802.1Q)
- OSPF (Area 0)
- EIGRP (AS 100)
- ACLs (standard and extended)
- Route redistribution
- Layer 3 subinterfaces

---

## How to Use

1. Open `secure_network_lab.pkt` in Cisco Packet Tracer
2. View device configurations in `router-configs/` and `switch-configs/`
3. Test connectivity:
   - ✅ PC1 → Server0 (allowed)
   - ❌ PC2/PC3/PC4 → Server0 (denied)
4. Use `tracert` or CLI commands like `show ip route` to explore routing paths


