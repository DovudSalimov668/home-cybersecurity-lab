# Home Cybersecurity Lab

## Overview

This repository documents my personal VMware-based cybersecurity lab. The lab was built to gain practical experience in networking, Linux administration, Windows administration, service enumeration, packet analysis, documentation, and security assessment methodologies.

The objective is to move beyond theory and create a repeatable environment where concepts can be tested, documented, and improved through hands-on practice.

The environment currently contains four virtual machines:

* Kali Linux (administration and testing workstation)
* Ubuntu Server (Linux server)
* Windows 11 Enterprise Evaluation (client workstation)
* Metasploitable 2 (intentionally vulnerable target)

The lab uses a segmented network design consisting of:

* Host-Only network for isolated internal communication
* NAT network for internet access where required

Metasploitable 2 remains isolated from the internet and is only reachable from the Host-Only network.

---

# Lab Objectives

## Technical Objectives

* Learn VMware networking
* Learn Linux system administration
* Learn Windows administration
* Practice SSH administration
* Practice service enumeration
* Practice packet analysis using Wireshark
* Build repeatable security assessment workflows
* Learn professional documentation standards

## Portfolio Objectives

* Create evidence of practical cybersecurity work
* Demonstrate technical documentation skills
* Demonstrate networking knowledge
* Demonstrate enumeration methodology
* Demonstrate home lab design and maintenance

---

# Hardware Platform

## Host System

| Component  | Value                    |
| ---------- | ------------------------ |
| CPU        | Intel Core Ultra 9 275HX |
| RAM        | 32 GB DDR5               |
| Storage    | NVMe SSD                 |
| Hypervisor | VMware Workstation Pro   |
| Host OS    | Windows                  |

---

# Virtual Machine Inventory

## Kali Linux

### Purpose

Primary administration and testing workstation.

### Resources

| Resource          | Value     |
| ----------------- | --------- |
| RAM               | 3 GB      |
| CPU               | 4 vCPU    |
| Disk              | 80 GB     |
| Network Adapter 1 | Host-Only |
| Network Adapter 2 | NAT       |

### Installed Tools

* Nmap
* Wireshark
* Zenmap
* Gobuster
* Feroxbuster
* Netcat
* Cryptcat

---

## Ubuntu Server

### Purpose

Linux server used for administration practice, SSH access, Apache deployment, and future logging exercises.

### Resources

| Resource          | Value     |
| ----------------- | --------- |
| RAM               | 4 GB      |
| CPU               | 2 vCPU    |
| Disk              | 30 GB     |
| Network Adapter 1 | Host-Only |
| Network Adapter 2 | NAT       |

### Active Services

* SSH
* Apache HTTP Server

---

## Windows 11 Enterprise Evaluation

### Purpose

Windows administration and endpoint practice workstation.

### Resources

| Resource          | Value     |
| ----------------- | --------- |
| RAM               | 8.3 GB    |
| CPU               | 4 vCPU    |
| Disk              | 70 GB     |
| Network Adapter 1 | Host-Only |
| Network Adapter 2 | NAT       |

---

## Metasploitable 2

### Purpose

Intentionally vulnerable training target.

### Resources

| Resource          | Value     |
| ----------------- | --------- |
| RAM               | 512 MB    |
| CPU               | 1 vCPU    |
| Disk              | 8 GB      |
| Network Adapter 1 | Host-Only |
| Network Adapter 2 | Host-Only |

### Notes

This machine intentionally exposes numerous vulnerable services and exists solely for educational practice inside the isolated lab environment.

---

# Network Architecture

## Host-Only Network

Subnet:

192.168.248.0/24

Purpose:

Internal communication between lab systems.

### Hosts

| System           | IP Address      |
| ---------------- | --------------- |
| Windows 11       | 192.168.248.128 |
| Ubuntu Server    | 192.168.248.130 |
| Kali Linux       | 192.168.248.131 |
| Metasploitable 2 | 192.168.248.132 |

---

## NAT Network

Subnet:

192.168.198.0/24

Purpose:

Internet access and package updates.

### Hosts

| System        | IP Address      |
| ------------- | --------------- |
| Ubuntu Server | 192.168.198.132 |
| Kali Linux    | 192.168.198.133 |
| Windows 11    | 192.168.198.134 |

---

# Repository Structure

```text
home-cybersecurity-lab/
├── diagrams/
├── docs/
├── reports/
├── scans/
├── screenshots/
├── scripts/
├── README.md
├── CHANGELOG.md
└── .gitignore
```

# Current Progress

## Completed

* VMware installation
* Virtual machine deployment
* Host-Only network configuration
* NAT network configuration
* Ubuntu SSH setup
* Ubuntu Apache setup
* Initial Nmap enumeration
* Git repository initialization
* GitHub repository creation
* Documentation structure creation

## Planned

* Wireshark traffic analysis
* Service discovery documentation
* Network diagrams
* Security assessment reports
* Log collection exercises
* Windows hardening exercises
* Ubuntu hardening exercises
* Monitoring experiments

---

# Disclaimer

This repository is intended exclusively for educational and defensive cybersecurity learning within a controlled virtual lab environment.

No testing should be performed against systems without authorization.
