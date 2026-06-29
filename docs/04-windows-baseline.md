# Windows 11 Baseline

## Purpose

Windows 11 serves as the primary workstation endpoint within the lab.

The system is used for:

* Windows administration
* Endpoint configuration
* Security monitoring
* Future Active Directory integration
* Logging experiments

---

# System Information

## Hostname

WIN11-LAB

## User

dovud

## Operating System

Microsoft Windows 11 Enterprise Evaluation

## Build

26200

---

# Hardware Allocation

| Resource | Value  |
| -------- | ------ |
| RAM      | 8.3 GB |
| CPU      | 4 vCPU |
| Disk     | 70 GB  |

---

# Network Adapters

## Ethernet0

Role:

Host-Only

Address:

192.168.248.128

Subnet:

255.255.255.0

Purpose:

Internal lab communication

---

## Ethernet1

Role:

NAT

Address:

192.168.198.134

Subnet:

255.255.255.0

Gateway:

192.168.198.2

Purpose:

Internet access

---

# DNS Configuration

## Host-Only Adapter

DNS:

192.168.248.1

---

## NAT Adapter

DNS:

192.168.198.2

---

# DHCP Configuration

Status:

Enabled

Assessment:

Addresses assigned automatically through VMware DHCP services.

---

# Security Observations

## ICMP Behavior

During testing the system appeared offline during certain scans.

Investigation determined:

Windows Firewall likely blocks ICMP echo requests.

Conclusion:

Lack of ping response does not indicate system failure.

---

# Network Analysis

## Internal Connectivity

Connected to:

* Kali Linux
* Ubuntu Server
* Metasploitable 2

through Host-Only networking.

---

## External Connectivity

Connected to:

* Internet
* Package repositories
* Browser access

through VMware NAT.

---

# Planned Security Enhancements

## Microsoft Sysmon

Purpose:

Advanced endpoint telemetry.

---

## Windows Event Forwarding

Purpose:

Centralized log collection.

---

## PowerShell Logging

Purpose:

Detection and analysis exercises.

---

## Windows Defender Analysis

Purpose:

Security monitoring practice.

---

# Future Role

This machine will eventually become:

* AD Client
* Log Source
* Detection Engineering Target
* Security Monitoring Endpoint

as the lab expands.
