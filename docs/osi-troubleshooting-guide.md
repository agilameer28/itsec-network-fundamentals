# Enterprise OSI Model Troubleshooting Guide

**Purpose:** Quick-reference mapping of the Open Systems Interconnection (OSI) model to aid in systematic network troubleshooting and incident response. 

**Core Troubleshooting Rule:** *Always verify Layer 1 (Physical) before spending hours troubleshooting Layer 7 (Application).*

---

## 🔼 Upper Layers (Host / Application Focused)

### Layer 7: Application
* **Function:** The interface between the network and the application software. Where the user interacts with data.
* **Protocol Data Unit (PDU):** Data
* **Protocols:** HTTP/HTTPS, DNS, FTP, SMTP, SSH
* **Devices/Services:** Web Browsers, Next-Gen Firewalls (Layer 7 filtering), Proxies
* **Troubleshooting Context:** "Is the website down, or is DNS failing to resolve the domain name?"

### Layer 6: Presentation
* **Function:** Data formatting, translation, encryption, and compression.
* **PDU:** Data
* **Protocols:** SSL/TLS, ASCII, JPEG, MPEG
* **Troubleshooting Context:** "Are we getting an SSL certificate error? Is the data encrypted properly?"

### Layer 5: Session
* **Function:** Establishes, maintains, and terminates connections between applications.
* **PDU:** Data
* **Protocols:** NetBIOS, RPC, PAP
* **Troubleshooting Context:** "Is the connection timing out or dropping prematurely?"

---

## 🔽 Lower Layers (Media / Network Focused)

### Layer 4: Transport
* **Function:** Reliable (TCP) or unreliable (UDP) delivery of data across a network. Handles port numbers and error recovery.
* **PDU:** Segments (TCP) / Datagrams (UDP)
* **Protocols:** TCP, UDP
* **Devices/Services:** Load Balancers, Stateful Firewalls
* **Troubleshooting Context:** "Is port 443 open? Is the firewall blocking TCP traffic to this server?"

### Layer 3: Network
* **Function:** Logical addressing and routing. Determines the best path for data to travel across different networks.
* **PDU:** Packets
* **Protocols:** IPv4, IPv6, ICMP, IPsec
* **Devices/Services:** Routers, Layer 3 Switches
* **Troubleshooting Context:** "Can we ping the destination IP? Is the routing table sending packets to the correct default gateway?"

### Layer 2: Data Link
* **Function:** Physical addressing (MAC addresses) and transferring data between two nodes on the same local network (LAN).
* **PDU:** Frames
* **Protocols:** Ethernet, ARP, VLANs (802.1Q)
* **Devices/Services:** Network Switches, Wireless Access Points (WAPs), Network Interface Cards (NICs)
* **Troubleshooting Context:** "Is the device on the correct VLAN? Do we have a MAC address conflict?"

### Layer 1: Physical
* **Function:** The physical media transmitting raw bits over a communication channel.
* **PDU:** Bits
* **Protocols:** 1000BASE-T, 802.11 (Wi-Fi physical transmission)
* **Devices/Services:** Cables (Cat6, Fiber), Hubs, Repeaters
* **Troubleshooting Context:** "Is the ethernet cable plugged in? Is the port on the switch lit up?"
