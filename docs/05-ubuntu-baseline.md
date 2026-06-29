# Ubuntu Server Baseline

## Purpose

Ubuntu Server functions as the primary Linux server within the Home Cybersecurity Lab.

The system provides a platform for:

* Linux administration practice
* SSH management
* Web server administration
* Service monitoring
* Security hardening exercises
* Log analysis

---

# System Information

## Hostname

ubuntu-lab

## Primary User

dovud

## Operating System

Ubuntu 26.04 LTS

## Kernel Version

7.0.0-14-generic

## Architecture

x86_64

## Virtualization

VMware Virtual Platform

---

# Hardware Allocation

| Resource | Value   |
| -------- | ------- |
| RAM      | 4096 MB |
| CPU      | 2 vCPU  |
| Disk     | 30 GB   |

---

# Network Configuration

## Interface: ens33

Purpose:

Host-Only communication

IP Address:

192.168.248.130

Subnet:

255.255.255.0

Role:

Internal lab communication

---

## Interface: ens37

Purpose:

NAT connectivity

IP Address:

192.168.198.132

Subnet:

255.255.255.0

Role:

Internet access

---

# Routing Analysis

## Default Route

Gateway:

192.168.198.2

Interface:

ens37

Purpose:

Internet access

---

## Internal Route

Network:

192.168.248.0/24

Interface:

ens33

Purpose:

Internal communication with lab systems

---

# Running Services

## SSH Service

Status:

Running

Port:

22/TCP

Purpose:

Remote administration

Verification:

SSH connection successfully established from Kali Linux.

---

## Apache HTTP Server

Status:

Running

Port:

80/TCP

Purpose:

Web service hosting

Verification:

Apache service confirmed active.

---

# Open Ports

Based on service inspection:

| Port | Service |
| ---- | ------- |
| 22   | SSH     |
| 80   | HTTP    |

---

# Installed Administrative Packages

Verified Packages:

* openssh-server
* apache2
* curl
* wget
* git
* vim
* htop
* net-tools
* fail2ban

---

# Security Analysis

## Strengths

### SSH Enabled

Allows secure administration.

### Fail2Ban Installed

Provides basic protection against brute-force attempts.

### Minimal Service Exposure

Only necessary services are exposed.

### Segmented Networking

Internal and external traffic separated.

---

## Risks

### Apache Running

Every exposed web service increases attack surface.

### Password Authentication

SSH password authentication may be less secure than key-based authentication.

### Default Configuration

Apache currently appears to be running with mostly default settings.

---

# Validation Performed

## SSH Access

Source:

Kali Linux

Destination:

Ubuntu Server

Result:

Successful.

---

## Service Verification

Commands Used

```bash
systemctl status ssh
systemctl status apache2
```

Result:

Both services active.

---

# Future Hardening Tasks

## SSH Hardening

* Disable root login
* Use key-based authentication
* Restrict users

## Apache Hardening

* Hide version information
* Configure security headers
* Enable logging review

## Firewall

* Configure UFW
* Limit exposed services

## Monitoring

* Audit logs
* Authentication logs
* Service monitoring

---

# Baseline Conclusion

Ubuntu Server is operational and correctly integrated into the lab architecture.

The system currently functions as a secure administration and web hosting platform while providing opportunities for future hardening exercises.
