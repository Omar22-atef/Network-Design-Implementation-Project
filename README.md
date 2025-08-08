# 📡 Network Design & Implementation Project

## 🎯 Project Objectives
Design, configure, and verify a **complex enterprise network** with multiple branches, VLANs, routing protocols, DHCP, NAT, VPN, and wireless connectivity.  
The goal is to ensure **full functionality**, **security**, and **efficient management**.

---

## 📋 Project Breakdown

| Part | Task | Weight |
|------|------|--------|
| 1 | Design & Implement VLSM Addressing Scheme | 10% |
| 2 | Build Network & Configure Basic Device Settings | 10% |
| 3 | Configure Layer 2 (VLANs, Trunking, Inter-VLAN Routing) | 10% |
| 4 | Configure Routing Protocols (OSPF, EIGRP, Redistribution) | 10% |
| 5 | Configure DHCP Server | 5% |
| 6 | Configure NAT (Dynamic NAT with PAT & Static NAT) | 5% |
| 7 | Configure Network Management (NTP, Syslog, DNS, Web & Email Servers) | 10% |
| 8 | Configure & Verify Site-to-Site IPsec VPN | 10% |
| 9 | Configure Wireless Home Router | 10% |
| 10 | Verify Full Network Connectivity | 10% |
| 11 | Documentation & Handover | 10% |

---

## 🏫 Background / Scenario
You are tasked with designing and implementing a **network for Misr International University (MIU)**.

**Requirements include:**
- **VLSM Addressing:** Efficient subnetting of `10.0.0.0/8`.
- **Layer 2 & 3 Configuration:** VLANs, trunking, EtherChannel, Inter-VLAN routing.
- **Routing:** OSPF & EIGRP with redistribution.
- **Network Services:** DHCP, NAT, NTP, Syslog, DNS, Web & Email servers.
- **Security:** Site-to-Site IPsec VPN and WPA2 wireless network.
- **Verification:** Full connectivity tests, routing verification, documentation.

---

## 🛠 Implementation Steps

<details>
<summary>📍 <b>Part 1: VLSM Addressing Scheme</b></summary>

- Subnet `10.0.0.0/8` based on host requirements.
- Fill in **Subnet Table** and **Addressing Table**.
</details>

<details>
<summary>📍 <b>Part 2: Basic Device Configuration</b></summary>

- Set hostnames.
- Set passwords:
  - Console: `MIU1234567`
  - Secret: `CSC1234567`
- Configure **SSH** for secure access.
- Apply **MOTD** banner.
- Assign IP addresses per Addressing Table.
</details>

<details>
<summary>📍 <b>Part 3: Layer 2 & Inter-VLAN Routing</b></summary>

- Create VLANs on all switches.
- Configure trunking (802.1Q).
- Set up **Inter-VLAN routing** on L3 switches.
- Configure **LACP EtherChannel** for redundancy.
</details>

<details>
<summary>📍 <b>Part 4: Routing Protocols</b></summary>

- **OSPF (Process ID: 100):** MIU-GW, Main-MLS, S-MLS.
- **EIGRP (AS 10):** MIU-GW, N-MLS, R-MLS.
- **Redistribute** between OSPF & EIGRP.
- Configure static & default routes for ISP connectivity.
</details>

<details>
<summary>📍 <b>Part 5: DHCP Configuration</b></summary>

**Main Branch:**
- Exclude first 3 IPs per VLAN.
- Configure DHCP pools for VLANs `100`, `200`, `300`, `400`.
- Set DHCP relay on Main-MLS & S-MLS.

**Branch:**
- Exclude first 5 IPs.
- Create pools `B-LAN2` & `B-LAN3`.
</details>

<details>
<summary>📍 <b>Part 6: NAT Configuration</b></summary>

- Dynamic NAT with PAT (`209.165.200.226`).
- Static NAT for `miu.edu.eg` (`209.165.200.227`).
- Verify NAT translations.
</details>

<details>
<summary>📍 <b>Part 7: Network Management</b></summary>

- Configure **NTP** for time sync.
- Set up **Syslog** logging.
- Configure **DNS** (`miu.edu.eg` → Web Server IP).
- Deploy Web Server (MIU logo homepage).
- Configure Email Server (`@miu.edu.eg`).
</details>

<details>
<summary>📍 <b>Part 8: Site-to-Site IPsec VPN</b></summary>

- Configure VPN between **MIU-GW** and **Branch-GW**.
- Verify encrypted traffic.
</details>

<details>
<summary>📍 <b>Part 9: Wireless Configuration</b></summary>

- **SSID:** `MIU-CSC230` (2.4 GHz).
- **Security:** WPA2-Personal (`miu_csc230`).
- Test connectivity with wireless clients (Laptop, Tablet, Smartphone).
</details>

<details>
<summary>📍 <b>Part 10: Verification</b></summary>

- Ping & traceroute tests between all devices.
- Routing Tables for all routers.
- NAT & VPN functionality checks.
</details>

<details>
<summary>📍 <b>Part 11: Documentation & Handover</b></summary>

Final Report (.docx or .pptx) with:
- All configurations.
- Screenshots (ping, traceroute, routing tables).
- Troubleshooting steps.
</details>

---

## ✅ Deliverables
- **Configuration files** (routers, switches, servers).
- **Testing screenshots** (connectivity, routing tables).
- **Final documentation** (step-by-step setup guide).

---

## 🏁 Conclusion
This project delivers a **fully functional enterprise network** with:
✔ Efficient **VLSM IP allocation**.  
✔ Redundant routing (**OSPF + EIGRP**).  
✔ Secure remote access (**IPsec VPN + WPA2**).  
✔ Automated IP assignment (**DHCP**).  
✔ Network monitoring (**NTP, Syslog, DNS**).
