# Lab Setup Documentation

## Purpose

This document records the initial deployment and configuration process of the Home Cybersecurity Lab.

Maintaining accurate setup documentation allows the environment to be rebuilt, audited, and improved over time.

---

# Hypervisor

## VMware Workstation

VMware Workstation is used as the virtualization platform.

Responsibilities:

* Virtual machine management
* Network segmentation
* Snapshot management
* Resource allocation

---

# Virtual Machine Deployment

## Kali Linux

### Configuration

RAM: 3104 MB

Processors: 4

Disk: 80.1 GB

Network Adapter 1:
Host-Only

Network Adapter 2:
NAT

### Purpose

Primary administration and assessment workstation.

---

## Ubuntu Server

### Configuration

RAM: 4096 MB

Processors: 2

Disk: 30 GB

Network Adapter 1:
Host-Only

Network Adapter 2:
NAT

### Purpose

Linux server used for SSH administration and web hosting.

---

## Windows 11 Enterprise Evaluation

### Configuration

RAM: 8500 MB

Processors: 4

Disk: 70 GB

Network Adapter 1:
Host-Only

Network Adapter 2:
NAT

### Purpose

Windows administration and workstation testing.

---

## Metasploitable 2

### Configuration

RAM: 512 MB

Processors: 1

Disk: 8 GB

Network Adapter 1:
Host-Only

Network Adapter 2:
Host-Only

### Purpose

Intentionally vulnerable target machine.

---

# Network Design

## Security Goal

Separate internet access from internal training traffic.

---

## Host-Only Network

Subnet:

192.168.248.0/24

Purpose:

* Internal communication
* Enumeration practice
* Packet analysis
* Service discovery

Connected Systems:

* Kali Linux
* Ubuntu Server
* Windows 11
* Metasploitable 2

---

## NAT Network

Subnet:

192.168.198.0/24

Purpose:

* Package updates
* Tool installation
* Internet connectivity

Connected Systems:

* Kali Linux
* Ubuntu Server
* Windows 11

Excluded Systems:

* Metasploitable 2

Reason:

Metasploitable 2 remains isolated from external networks to reduce risk and maintain a controlled training environment.

---

# Validation

## Ubuntu SSH Test

Source:

Kali Linux

Destination:

Ubuntu Server

Result:

Successful authentication and shell access confirmed.

---

## Ubuntu Apache Test

Service:

Apache HTTP Server

Port:

80/TCP

Result:

Running successfully.

---

## Network Validation

Verified:

* Host-Only communication
* NAT internet access
* DHCP functionality
* Routing functionality

---

# Initial Tool Installation

## Kali Linux

Verified Installed:

* Nmap
* Zenmap
* Wireshark
* Gobuster
* Feroxbuster
* Netcat
* Cryptcat

## Ubuntu Server

Verified Installed:

* OpenSSH Server
* Apache2
* Net-Tools
* Curl
* Wget
* Git
* Vim
* Htop
* Fail2Ban

---

# Current State

The environment is operational and ready for:

* Network enumeration
* Service discovery
* Packet analysis
* Documentation exercises
* Security assessment practice
