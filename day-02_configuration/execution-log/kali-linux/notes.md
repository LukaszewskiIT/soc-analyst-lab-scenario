# Day 2 – Kali Linux: System Update & Network Configuration

## 🔧 System Update

Logged into the Kali Linux machine as root.

Executed the following command to update all packages:

```bash
sudo apt update && sudo apt upgrade -y
```

This command:
- Refreshes the package list
- Installs all available updates
- Ensures the system is secure and up-to-date for further lab usage

![System update](../screenshots/kali-update.png)

---

## 🌐 Network Adapter Check

Verified VirtualBox network settings:

- **Adapter Type**: NAT  
- **Model**: Intel PRO/1000 MT Desktop

This adapter type gives Kali internet access but keeps it logically outside the internal network.

![VBox adapter](../screenshots/kali-vbox-network.png)

---

## 🛜 Static IP Assignment

Configured a static IP address to ensure consistent communication throughout the lab scenario.

Opened the config file:

```bash
sudo nano /etc/network/interfaces
```

Added the following:

```
auto eth0
iface eth0 inet static
  address 192.168.100.100
  netmask 255.255.255.0
  gateway 192.168.100.1
```

Restarted the networking service:

```bash
sudo systemctl restart networking
```

Confirmed the IP assignment with:

```bash
ip a
```

![Interfaces file](../screenshots/kali-ip-config-file.png)  
![IP check](../screenshots/kali-ip-check.png)

---

## 💭 Notes

- System was successfully updated and ready for attack operations  
- Static IP set to `192.168.100.100` for predictable routing  
- Internet access retained via NAT adapter  
- This machine now simulates an external attacker node with outbound connectivity only
