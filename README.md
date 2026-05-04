# Enterprise Hybrid Network: Site-to-Site VPN & VoIP Implementation

## 🌐 Overview
This project demonstrates a complex enterprise network architecture built in **Cisco Packet Tracer**. It bridges a remote Home Office with a Corporate HQ through a simulated ISP, ensuring secure communication and integrated services.

## 🛠️ Key Implementations

### 1. Secure Remote Access (VPN)
* **IPsec Site-to-Site VPN:** Configured a secure tunnel between the Home Office (192.168.10.0/24) and HQ (10.0.0.0/8).
* **Mirror ACL Strategy:** Implemented symmetrical Access Control Lists to identify and trigger encryption.
* **ISP Integration:** Managed routing across a simulated ISP core to maintain connectivity.

### 2. Advanced Networking & Segregation
* **VLAN Architecture:** Segmented the office into 5 distinct VLANs (Management, Marketing, Voice, etc.) for optimized broadcast domains.
* **Inter-VLAN Routing:** Router-on-a-Stick configuration.
* **DHCP Services:** Centralized IP management with specialized **Option 150** for VoIP auto-configuration.

### 3. Voice over IP (VoIP)
* **Telephony Service:** Configured ephone-dn registration.
* **QoS Basics:** Voice VLAN tagging to prioritize real-time traffic over data.

## 🔍 The Troubleshooting Journey (The "Net" Edge)
The core of this project was solving real-world-style failures:
* **IP Conflict Resolution:** Fixed a major routing loop by re-addressing the home network from the 10.0.0.0 range to 192.168.10.0.
* **Asymmetric Routing:** Debugged and corrected ISP static routes that caused "Destination Unreachable" errors.
* **STP Optimization:** Applied `spanning-tree portfast` to ensure IP phones register immediately without timeouts.

## 📁 Repository Content
* `Network_Architecture.pkt`: The complete lab environment.
* `/Documentation`: Running configurations and logic diagrams.
* `/Verification`: Screenshots of successful VPN tunnels and VoIP registration.

---
*Created as a hands-on lab for Networking & Security.*
