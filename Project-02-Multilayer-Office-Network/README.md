# 🌐 Project 01 – Enterprise Campus Network

## 📖 Project Overview

This project simulates a real-world **Enterprise Campus Network** using Cisco Packet Tracer. The network follows a hierarchical design consisting of an Enterprise Router, two Multilayer Switches (Core Layer), four Access Switches, multiple VLANs, centralized DHCP services, OSPF dynamic routing, EtherChannel, NAT, and ACLs.

The objective of this project is to demonstrate enterprise-level LAN design, secure inter-VLAN communication, dynamic routing, Internet connectivity, and traffic control using Cisco networking technologies.

---

# 🏗️ Network Topology

The complete enterprise topology is shown below.

![Network Topology](Screenshots/00-topology-overview.png)

---

# 🎯 Project Objectives

 Design a scalable Enterprise Campus Network
 Configure multiple VLANs for different departments
 Configure Trunk links between Access and Core switches
 Configure EtherChannel between Core Switches
 Configure SVIs for Inter-VLAN Routing
 Configure OSPF Dynamic Routing
 Configure Centralized DHCP Services
 Configure NAT for Internet Access
 Configure ACLs for Guest VLAN Security
 Verify end-to-end communication between VLANs

---

# 🛠️ Technologies Used

 Cisco Packet Tracer
 VLANs
 IEEE 802.1Q Trunking
 Multilayer Switching
 Switch Virtual Interfaces (SVIs)
 OSPF
 EtherChannel (LACP)
 DHCP
 NAT
 ACL
 Static Default Route

---

# 🖥️ Network Architecture

### Enterprise Router

 Connects the enterprise network to the ISP
 Performs NAT
 Advertises routes using OSPF
 Provides Internet connectivity

### Core Layer

 MLS1
 MLS2

Responsibilities:

 Inter-VLAN Routing
 OSPF Routing
 EtherChannel
 DHCP Relay
 High-speed backbone connectivity

### Access Layer

 SW1
 SW2
 SW3
 SW4

Responsibilities:

 VLAN segmentation
 End device connectivity
 Trunk uplinks to Core

---

# 🏢 VLAN Configuration

The network contains six VLANs.

| VLAN    | Department |
|---------|------------|
| VLAN 10 | HR         |
| VLAN 20 | Finance    |
| VLAN 30 | Sales      |
| VLAN 40 | IT         |
| VLAN 50 | Management |
| VLAN 60 | Guest      |

---

## SW1 VLAN Configuration

![SW1 VLAN](Screenshots/01-vlan-brief-sw1.png)

---

## SW2 VLAN Configuration

![SW2 VLAN](Screenshots/02-vlan-brief-sw2.png)

---

## SW3 VLAN Configuration

![SW3 VLAN](Screenshots/03-vlan-brief-sw3.png)

---

## SW4 VLAN Configuration

![SW4 VLAN](Screenshots/04-vlan-brief-sw4.png)

---

# 🔗 Trunk Configuration

Trunk links were configured between the Access Switches and Core Switches to allow multiple VLANs across a single physical connection.

## MLS1 Trunk Ports

![MLS1 Trunk](Screenshots/05-trunk-mls1.png)

---

## MLS2 Trunk Ports

![MLS2 Trunk](Screenshots/06-trunk-mls2.png)

---

# ⚡ EtherChannel Configuration

LACP EtherChannel was configured between MLS1 and MLS2 to provide:

 Redundancy
 Increased Bandwidth
 Load Balancing

Verification:

![EtherChannel](Screenshots/07-etherchannel-summary.png)

---

# 🌐 Inter-VLAN Routing (SVIs)

Inter-VLAN Routing is performed on the Multilayer Switches using Switch Virtual Interfaces (SVIs).

## MLS1 SVIs

![MLS1 SVI](Screenshots/08-svi-mls1.png)

---

## MLS2 SVIs

![MLS2 SVI](Screenshots/09-svi-mls2.png)

---

# 📡 DHCP Configuration

Centralized DHCP services were configured to dynamically assign IP addresses to all VLANs.

Verification:

![DHCP Bindings](Screenshots/10-dhcp-bindings.png)

---

# 🛰️ Dynamic Routing (OSPF)

OSPF was configured between:

 Enterprise Router
 MLS1
 MLS2

This allows automatic route advertisement throughout the network.

---

# 🛣️ Routing Table Verification

## Enterprise Router

![Enterprise Routing Table](Screenshots/11-routing-table-enterprise.png)

---

## MLS1 Routing Table

![MLS1 Routing Table](Screenshots/12-routing-table-mls1.png)

---

# 🌍 NAT Configuration

Network Address Translation (NAT) was configured on the Enterprise Router to allow internal private IP addresses to communicate with external networks.

Features:

 PAT (Overload)
 Inside/Outside Interfaces
 Internet Access

---

# 🔐 Access Control Lists (ACL)

ACLs were configured to restrict traffic from the Guest VLAN while allowing authorized communication across the enterprise network.

---

# ✅ Connectivity Verification

## HR → Finance

Successful communication between HR and Finance VLAN.

![HR to Finance](Screenshots/13-ping-hr-to-finance.png)

---

## Sales → IT

Successful communication between Sales and IT VLAN.

![Sales to IT](Screenshots/14-ping-sales-to-it.png)

---

## HR → Management

Successful communication between HR and Management VLAN.

![HR to Management](Screenshots/15-ping-hr-to-management.png)

---


# 🎯 Skills Demonstrated

 Enterprise Network Design
 VLAN Implementation
 IEEE 802.1Q Trunking
 EtherChannel (LACP)
 Inter-VLAN Routing
 Switch Virtual Interfaces (SVIs)
 OSPF Dynamic Routing
 DHCP Configuration
 NAT Configuration
 ACL Configuration
 Internet Connectivity
 Routing Verification
 End-to-End Network Troubleshooting

---

# 📌 Conclusion

This project demonstrates the implementation of a scalable Enterprise Campus Network using Cisco networking technologies. It integrates Layer 2 and Layer 3 networking concepts including VLAN segmentation, Inter-VLAN Routing, EtherChannel, OSPF, DHCP, NAT, and ACLs to provide secure and efficient communication across the enterprise.

The successful verification of routing tables, VLAN communication, DHCP address allocation, and end-to-end connectivity confirms the correct operation of the network and highlights practical enterprise networking skills applicable to real-world environments.
