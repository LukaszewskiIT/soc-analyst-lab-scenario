# Day 1 – Virtual Lab Setup (Planning & Preparation)

## 🎯 Objective

The goal of this phase is to plan and prepare a virtual lab environment simulating a basic corporate network infrastructure, along with an external attacker machine (Kali Linux).  
This lab is built entirely in **VirtualBox** and will be used for a full **attack-and-defense simulation** later in the project.

The documentation aims to be clear and replicable — allowing **anyone to recreate the full experiment** on their own machine.

> 🔁 *Note: Some setup notes and parameters may be updated later during the execution phases, if adjustments or improvements are discovered.*

---

## 🌱 Planned Lab Structure

### 🏢 Internal Corporate Network
- **Windows 10 Workstation** – simulating an employee workstation
- **Debian Linux Server** – hosting a mock database with sensitive data
- **VPN Gateway (Linux)** – providing controlled internet access for internal hosts

### 🌐 External Attacker Machine
- **Kali Linux** – placed outside the internal network, simulating a real-world attacker

---

## 🛠️ Tasks for Today

- Install and configure **VirtualBox**
- Create virtual machines:
  - Windows 10
  - Debian Linux (latest stable version)
  - Kali Linux
  - Linux VPN Gateway
- Assign appropriate **resources** (RAM, CPU, disk) to each VM
- Configure **network interfaces**:
  - Internal LAN (host-only adapter)
  - NAT or bridged adapter for VPN Gateway only
  - Ensure proper isolation between external and internal systems

---

## 💬 Notes

This file will be updated as I progress through the setup process.  
Screenshots and configuration details will be added during and after implementation.  

The goal is to produce a well-documented, modular and reproducible lab that can be used for personal learning, training, or showcasing technical cybersecurity skills.
