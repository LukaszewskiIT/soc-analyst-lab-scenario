# Day 2 – Initial Configuration & Network Setup

## 🎯 Objective

The goal of Day 2 is to perform initial configuration of all virtual machines and establish secure, isolated networking between internal and external nodes.  
This step lays the groundwork for attack simulation and logging/monitoring.

---

## 🔧 Configuration Checklist

### ✅ General Tasks:
- [ ] Boot and verify all VMs launch correctly
- [ ] Set static IP addresses for internal nodes (Windows 10, Debian Server)
- [ ] Set hostname for each machine
- [ ] Configure `/etc/hosts` or DNS mappings if needed
- [ ] Update & upgrade system packages (where needed)

---

### 🛜 Networking Tasks:

#### 🏢 Internal LAN (Host-Only Adapter):
- [ ] Assign static IPs (e.g. 192.168.100.X/24)
- [ ] Ensure all internal machines can ping each other
- [ ] Disable internet access for Windows10 & Debian
- [ ] VPN Gateway will act as optional NAT device later

#### 🌐 External (Bridged/NAT):
- [ ] Kali Linux connected to NAT (external attacker)
- [ ] VPN Gateway — verify it connects externally via NAT/bridged
- [ ] Kali should **not** have access to internal LAN yet

---

## 🧪 Verification & Testing:

- [ ] Internal ping tests: Win10 ↔ Debian ↔ VPN Gateway
- [ ] External ping tests: Kali ↔ VPN Gateway
- [ ] Traceroute to verify routing paths
- [ ] Confirm isolation between external ↔ internal

---

## 📷 Screenshots to include:
- IP configuration screenshots for each host  
- Output of `ip a`, `ipconfig`, `ping`, `tracert/traceroute`  
- Routing table or `netstat -rn` from each VM  
- Kali failing to reach internal nodes (proof of initial isolation)

---

## 💬 Notes

At this stage, we are preparing the environment for the future attack simulation.  
The configuration may be adjusted later depending on detection/logging needs.  
All IPs and routing will be documented to ensure reproducibility of the scenario.
