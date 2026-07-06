# Network Security & Scanning

## ApexPlanet Software Pvt. Ltd. Internship - Task 2

---

# Project Overview

This project demonstrates the basic concepts of Network Security, Reconnaissance, Port Scanning, Vulnerability Assessment, Packet Analysis, and Firewall Configuration using Kali Linux.

The project was completed as part of the ApexPlanet Software Pvt. Ltd. Cyber Security Internship.

---

# Objectives

- Learn Passive and Active Reconnaissance
- Perform Network Scanning using Nmap
- Detect Services and Operating System
- Perform Vulnerability Assessment using OpenVAS
- Analyze Network Traffic using Wireshark
- Configure Firewall using iptables
- Document findings professionally

---

# Lab Environment

| Component | Details |
|-----------|----------|
| Operating System | Kali Linux |
| Target Machine | Metasploitable2 |
| Scanner | Nmap |
| Vulnerability Scanner | OpenVAS (Greenbone) |
| Packet Analyzer | Wireshark |
| Firewall | iptables |
| Virtualization | VMware Workstation / VirtualBox |

---

# Tools Used

- Kali Linux
- Metasploitable2
- Nmap
- OpenVAS (Greenbone)
- Wireshark
- iptables
- Terminal

---

# Project Structure

```
Network-Security-Scanning
│
├── README.md
├── OpenVAS_Report.pdf
│
└── screenshots
    ├── 01_metasploitable_ip.png
    ├── 02_whois.png
    ├── 03_nslookup.png
    ├── 04_ping.png
    ├── 05_nmap_tcp.png
    ├── 06_nmap_udp.png
    ├── 07_service_detection.png
    ├── 08_os_detection.png
    ├── 09_openvas_completed.png
    ├── 10_openvas_summary.png
    ├── 11_dns_filter.png
    ├── 12_http_filter.png
    └── 13_firewall.png
```

---

# Step 1 - Target IP Identification

Command

```bash
ifconfig
```

Purpose

Find the IP address of the Metasploitable2 machine which will be used as the target.

Screenshot

screenshots/01_ifconfig.png

---

# Step 2 - WHOIS Lookup

Command

```bash
whois google.com
```

Purpose

Collect publicly available domain registration information.

Output includes

- Registrar
- Domain Name
- Registration Date
- Name Servers

Screenshot

screenshots/02_whois.png

---

# Step 3 - DNS Lookup

Command

```bash
nslookup google.com
```

Purpose

Resolve the domain name into its IP address.

Screenshot

screenshots/03_nslookup.png

---

# Step 4 - Ping Test

Command

```bash
ping -c 4 192.168.xx.xxx
```

Purpose

Verify network connectivity between Kali Linux and Metasploitable2.

Screenshot

screenshots/04_ping.png

---

# Step 5 - TCP SYN Scan

Command

```bash
sudo nmap -sS 192.168.xx.xxx
```

Purpose

Identify open TCP ports.

Expected Output

- FTP
- SSH
- HTTP
- Telnet

Screenshot

screenshots/05_nmap_tcp.png

---

# Step 6 - UDP Scan

Command

```bash
sudo nmap -sU 192.168.xx.xxx
```

Purpose

Identify UDP services running on the target machine.

Screenshot

screenshots/06_nmap_udp.png

---

# Step 7 - Service Version Detection

Command

```bash
sudo nmap -sV 192.168.xx.xxx
```

Purpose

Detect versions of services running on open ports.

Screenshot

screenshots/07_service_detection.png

---

# Step 8 - Operating System Detection

Command

```bash
sudo nmap -O 192.168.xx.xxx
```

Purpose

Identify the operating system of the target machine.

Screenshot

screenshots/08_os_detection.png

---

# Step 9 - Vulnerability Assessment

Tool

OpenVAS (Greenbone)

Activities Performed

- Created Target
- Created Scan Task
- Executed Vulnerability Scan
- Generated Vulnerability Report

Screenshots

screenshots/09_openvas_completed.png

screenshots/10_openvas_summary.png

Generated Report

OpenVAS_Report.pdf

---

# Step 10 - Packet Analysis

Tool

Wireshark

Activities

Captured HTTP Traffic

Applied Filter

```text
http
```

Screenshot

screenshots/12_http_filter.png

---

Captured DNS Traffic

Applied Filter

```text
dns
```

Screenshot

screenshots/11_dns_filter.png

---

# Step 11 - Firewall Configuration

Command

```bash
sudo iptables -A INPUT -p tcp --dport 80 -j DROP
```

Verify Rule

```bash
sudo iptables -L
```

Purpose

Block incoming HTTP traffic on Port 80.

Screenshot

screenshots/13_firewall.png

---

# Reports

- OpenVAS_Report.pdf

---

# Key Learnings

- Passive Reconnaissance
- Active Reconnaissance
- Port Scanning
- Service Enumeration
- OS Fingerprinting
- Vulnerability Assessment
- Network Traffic Analysis
- Firewall Rule Configuration

---

# Conclusion

Successfully completed Network Security and Scanning tasks using Kali Linux, Nmap, OpenVAS, Wireshark, and iptables. The project demonstrates practical knowledge of reconnaissance, scanning, vulnerability assessment, packet analysis, and firewall configuration in a controlled lab environment.

---

# Author

**Sameer Singh**

Cyber Security Intern

ApexPlanet Software Pvt. Ltd.
