# Kali Linux Baseline

## Purpose

Kali Linux serves as the primary administration and security testing workstation within the lab.

It is used for:

* Enumeration
* Packet analysis
* Service discovery
* Documentation
* SSH administration

---

# System Information

## Hostname

kali

## Operating System

Kali GNU/Linux Rolling

## Version

2025.4

## Kernel

6.16.8+kali-amd64

## Architecture

x86_64

## Virtualization

VMware

---

# Hardware Allocation

| Resource | Value   |
| -------- | ------- |
| RAM      | 3104 MB |
| CPU      | 4 vCPU  |
| Disk     | 80.1 GB |

---

# Network Interfaces

## eth0

Role:

Host-Only

Address:

192.168.248.131/24

Purpose:

Internal lab communication

---

## eth1

Role:

NAT

Address:

192.168.198.133/24

Purpose:

Internet connectivity

---

# Routing Table

## Default Route

Destination:

0.0.0.0/0

Gateway:

192.168.198.2

Interface:

eth1

---

## Internal Route

Destination:

192.168.248.0/24

Interface:

eth0

Purpose:

Communication with lab systems

---

# Installed Security Tools

## Network Enumeration

* Nmap
* Zenmap

### Purpose

Port scanning and service discovery.

---

## Packet Analysis

* Wireshark

### Purpose

Traffic capture and protocol analysis.

---

## Content Discovery

* Gobuster
* Feroxbuster

### Purpose

Directory and content discovery.

---

## Networking Utilities

* Netcat
* Cryptcat

### Purpose

Network troubleshooting and TCP testing.

---

# Listening Services

Command Used

```bash
sudo ss -tulpn
```

Result:

No significant listening services identified.

Assessment:

Expected behavior for a workstation system.

---

# Security Assessment

## Strengths

* Modern operating system
* Updated toolset
* Dual-network design
* Minimal exposed services

## Risks

* Testing tools require careful use
* Misconfigured scans can create unnecessary traffic
* Packet captures may contain sensitive information

---

# Operational Notes

Kali acts as:

* Administrator workstation
* Scanning platform
* Documentation platform
* Traffic analysis workstation

No production services are hosted on Kali.

---

# Future Additions

Planned tools:

* Burp Suite
* OWASP Amass
* BloodHound
* Splunk Forwarder
* Sysmon Log Analysis
* Security Onion integrations
