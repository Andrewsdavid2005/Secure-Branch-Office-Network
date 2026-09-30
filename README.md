# Secure Branch Office Network

A secure and segmented **Branch Office Network** designed and implemented using **Cisco Packet Tracer**.

This project demonstrates practical enterprise networking concepts including **VLAN segmentation, Router-on-a-Stick, Inter-VLAN Routing, DHCP, Extended ACLs, SSH, Port Security, PortFast, and network troubleshooting**.

---

## Project Overview

The objective of this project is to design a small but secure branch-office network where different departments are logically separated using VLANs.

The network implements:

- VLAN segmentation
- Inter-VLAN routing
- Router-on-a-Stick
- DHCP
- Extended ACL
- SSH remote management
- Switch Port Security
- Sticky MAC address learning
- PortFast
- Network troubleshooting
- Cisco IOS verification

The project simulates a real-world branch office containing **HR, IT, Guest users, and a server**.

---

## Project Objectives

The main objectives of this project are:

1. Design a structured branch-office network.
2. Separate departments using VLANs.
3. Configure Inter-VLAN Routing using Router-on-a-Stick.
4. Automatically assign IP addresses using DHCP.
5. Restrict Guest users from accessing the IT network using ACLs.
6. Secure router management using SSH.
7. Protect switch access ports using Port Security.
8. Practice network troubleshooting.
9. Verify network connectivity using Cisco IOS commands.
10. Develop practical Cisco networking skills using Packet Tracer.

---

# Network Topology

## Devices Used

| Device | Quantity |
|---|---:|
| Cisco 2911 Router | 1 |
| Cisco 2960 Switch | 1 |
| PCs | 4 |
| Server | 1 |

---

## Logical Topology

```text
                         ┌─────────────────────┐
                         │       BR-R1          │
                         │     Cisco 2911       │
                         │                      │
                         │ Router-on-a-Stick    │
                         └──────────┬──────────┘
                                    │
                              802.1Q Trunk
                                    │
                         ┌──────────┴──────────┐
                         │       BR-SW1        │
                         │      Cisco 2960     │
                         └───┬────┬────┬────┬──┘
                             │    │    │    │
                            PC1  PC2  PC3  PC4
                             │    │    │    │
                          VLAN10 VLAN20 VLAN30
                            HR     IT    GUEST
                                      │
                                  ┌───┴────┐
                                  │ Server │
                                  │ .20.10│
                                  └────────┘
