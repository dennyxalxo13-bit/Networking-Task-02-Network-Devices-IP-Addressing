# Networking Task 02 — Network Devices & IP Addressing

**Author:** Denny Xalxo
**Task:** Networking Task 02
**Domain:** Computer Networking — Internship Assignment

---

##  Overview

This task dives deeper into computer networking by researching key network devices, classifying IP addresses as public or private, analyzing a real device's network environment, tracing the communication flow when browsing the web, and running practical diagnostic commands.

---

##  File Structure

```
Networking_Task_02_Denny_Xalxo.docx   # Main task submission document
README.md                              # This file
```

---

##  Task Breakdown

### Part A — Network Devices Research

A research-based explanation of six fundamental network devices:

| Device | Purpose | How It Works | Real-World Usage |
|--------|---------|--------------|-----------------|
| **Router** | Connects different networks and directs data packets | Uses IP addresses to forward data to the correct destination | Home Wi-Fi routers connecting devices to the internet |
| **Switch** | Connects multiple devices within the same network | Uses MAC addresses to send data only to the intended device | Offices, schools, and computer labs |
| **Hub** | Connects multiple devices in a network | Sends incoming data to all connected devices without filtering | Older networks; largely replaced by switches |
| **Access Point (AP)** | Provides wireless network access | Connects wireless devices to a wired network via Wi-Fi signals | Wi-Fi hotspots, offices, schools, and homes |
| **Firewall** | Protects a network from unauthorized access | Monitors and filters incoming/outgoing traffic, blocks threats | Organizations and personal computers for security |
| **Modem** | Connects a network to an ISP | Converts digital signals into signals compatible with ISP lines | Internet connections in homes and offices |

---

### Part B — IP Address Classification

Identification of IP addresses as Public or Private based on their ranges:

| IP Address | Type | Reason |
|------------|------|--------|
| `192.168.1.10` |  Private | Falls within the `192.168.0.0 – 192.168.255.255` range |
| `10.0.0.5` |  Private | Falls within the `10.0.0.0 – 10.255.255.255` range |
| `172.16.5.20` |  Private | Falls within the `172.16.0.0 – 172.31.255.255` range |
| `8.8.8.8` |  Public | Google's public DNS server |
| `1.1.1.1` |  Public | Cloudflare's public DNS server |
| `192.168.100.1` |  Private | Falls within the `192.168.0.0 – 192.168.255.255` range |

---

### Part C — Understanding Your Network

Analysis of the device's own network configuration:

- **IP Range:** `192.168.1.x`
- **IP Type:** Private (falls within the `192.168.x.x` range)
- **Router Role:** Connects the local network to the internet and directs data packets between devices and external networks
- **If DNS Stopped Working:** Websites would not load via domain names since DNS translates names to IP addresses; users would need to use raw IP addresses to access sites

---

### Part D — Network Communication Flow

Step-by-step breakdown of what happens when you visit `www.google.com`:

```
💻 Your Device
      ↓
📶 Router
      ↓
🗂️ DNS Server
      ↓
🖥️ Google Server
      ↓
📨 Response Back to Device
```

| Step | Stage | Description |
|------|-------|-------------|
| 1 | **User Request** | The browser sends a request when the user types `www.google.com` |
| 2 | **Router** | The router forwards the request from the local network to the internet |
| 3 | **DNS Server** | DNS resolves `www.google.com` into its corresponding IP address |
| 4 | **Google Server** | The request reaches Google's server using the resolved IP address |
| 5 | **Response** | Google's server sends the webpage data back through the internet and router to the user's device |

---

### Part E — Practical Command Exercise

Command-line tools used for network diagnostics on Windows:

```bash
ipconfig /all        # Displays full network configuration details
nslookup google.com  # Queries the DNS server to resolve a domain name
ping google.com      # Tests network connectivity and measures response time
```

**Results Summary:**

| Test | Result |
|------|--------|
| DNS-resolved IP for Google | `142.250.193.78` |
| Ping to google.com |  Successful — replies received |
| Why DNS matters | Converts human-readable domain names into IP addresses needed for communication |

---

## 🛠️ Tools & Commands Used

| Command | Purpose |
|---------|---------|
| `ipconfig /all` | View full network adapter configuration |
| `nslookup` | Query DNS servers for domain name resolution |
| `ping` | Test connectivity and measure round-trip latency |

---

##  Key Concepts Covered

- Network devices: Router, Switch, Hub, Access Point, Firewall, Modem
- Public vs. Private IP address ranges (RFC 1918)
- DNS resolution and its role in web communication
- Network communication flow (client → router → DNS → server → response)
- Practical network diagnostics using Windows CLI tools

---

##  About

This is an internship assignment focused on building foundational knowledge in computer networking. The task combines device research, IP classification theory, and hands-on command-line diagnostics to reinforce core networking concepts.
