# Enterprise Campus Network Design & Configuration (3-Tier Architecture)

An enterprise-grade, highly available 3-Tier Campus Network built and simulated in **Cisco Packet Tracer**. This project demonstrates complete network redundancy, inter-VLAN routing, high-availability switching, floating static routes, and Dynamic NAT/PAT for WAN reachability.

---

## 📸 Network Topology

![Network Topology](Screenshot%202026-07-21%20195309.png)

---

## 🛠️ Architecture Highlights & Features

* **3-Tier Hierarchical Design:** Core, Distribution, and Access Layer separation for enterprise scalability.
* **Link Redundancy & Aggregation:** LACP EtherChannels implemented between Access and Distribution layers.
* **Spanning Tree Protocol (STP):** Rapid PVST+ configured with primary/secondary root bridges per VLAN for loop-free paths and load sharing.
* **Inter-VLAN & L3 Routing:** Core and Distribution L3 Switches handling SVI routing and inter-subnet traffic.
* **Redundant Pathing:** Primary static default routes backed by **Floating Static Routes** (Metric 10) across cross-links.
* **Edge Security & NAT:** Dynamic NAT / PAT Overload configured on `EDGE-RT` to translate internal traffic to simulated WAN endpoints.

---

## 🌐 IP & Subnet Schemes

| Device / Interface | Subnet / Role | IP Address / Configuration |
| :--- | :--- | :--- |
| **VLAN 10** | Clients Subnet A | `10.10.0.0/24` (GW: `10.10.0.1`) |
| **VLAN 20** | Clients Subnet B | `10.21.0.0/24` (GW: `10.21.0.1`) |
| **DIST-SW1 / DIST-SW2** | L3 Inter-Core / SVIs | Active/Backup Gateway Redundancy |
| **CORE-SW1 / CORE-SW2** | Layer 3 Core Routing | `10.255.x.x/30` Point-to-Point Links |
| **EDGE-RT (Gi0/0/2)** | Outside WAN Interface | Public Subnet / Simulated ISP |

---

## 📁 Repository Structure

```text
.
├── ACC-SW1.txt                           # Access Switch 1 CLI Commands
├── ACC-SW2.txt                           # Access Switch 2 CLI Commands
├── DIST-SW1.txt                          # Distribution Switch 1 CLI Commands
├── DIST-SW2.txt                          # Distribution Switch 2 CLI Commands
├── CORE-SW1.txt                          # Core Switch 1 CLI Commands
├── CORE-SW2.txt                          # Core Switch 2 CLI Commands
├── EDGE ROUTER.txt                       # Edge Router NAT & Routing Script
├── Enterprise_Campus_Network_v1.pkt      # Cisco Packet Tracer Lab File
└── Screenshot 2026-07-21 195309.png      # Network Topology Diagram

```text

## 👤 Author

**Tishan Nilusha**
*Cybersecurity Student | Exploring Web Security, Ethical Hacking & Network Security*
