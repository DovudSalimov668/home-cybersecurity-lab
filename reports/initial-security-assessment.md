# Initial Security Assessment Report

## Executive Summary

A VMware-based cybersecurity lab environment was assessed to verify configuration, connectivity, service exposure, and operational readiness.

The environment contains:

* Kali Linux
* Ubuntu Server
* Windows 11 Enterprise Evaluation
* Metasploitable 2

The assessment confirms that network segmentation is functioning correctly and the environment is ready for further security learning activities.

---

# Assessment Scope

Included Systems:

| System           | Role                       |
| ---------------- | -------------------------- |
| Kali Linux       | Administration and testing |
| Ubuntu Server    | Linux server               |
| Windows 11       | Client workstation         |
| Metasploitable 2 | Vulnerable target          |

---

# Methodology

The assessment included:

* Host discovery
* Network validation
* Route verification
* Service identification
* Configuration review
* Documentation review

Tools used:

* Nmap
* SSH
* Linux networking utilities
* Windows networking utilities

---

# Findings

## Finding 1

### Title

Network Segmentation Successfully Implemented

### Severity

Informational

### Description

The environment uses separate Host-Only and NAT networks.

### Impact

Reduces risk of accidental interaction with external systems.

### Status

Verified

---

## Finding 2

### Title

Ubuntu Server Operational

### Severity

Informational

### Description

SSH and Apache services are active and accessible.

### Impact

Provides stable platform for administration exercises.

### Status

Verified

---

## Finding 3

### Title

Windows Endpoint Operational

### Severity

Informational

### Description

Windows 11 correctly participates in both network segments.

### Impact

Provides endpoint platform for future monitoring exercises.

### Status

Verified

---

## Finding 4

### Title

Metasploitable 2 Exposes Multiple Legacy Services

### Severity

Expected

### Description

Numerous services are intentionally exposed.

### Impact

Provides realistic enumeration and assessment opportunities.

### Status

Verified

---

# Risk Overview

| System           | Exposure Level     |
| ---------------- | ------------------ |
| Kali Linux       | Low                |
| Ubuntu Server    | Low                |
| Windows 11       | Low                |
| Metasploitable 2 | High (Intentional) |

---

# Recommendations

## Short-Term

* Complete documentation
* Store scan evidence
* Capture screenshots
* Create architecture diagrams

## Medium-Term

* Configure UFW on Ubuntu
* Configure Sysmon on Windows
* Establish centralized logging

## Long-Term

* Add Active Directory
* Add SIEM platform
* Add monitoring infrastructure
* Add detection engineering exercises

---

# Overall Assessment

The lab is correctly segmented, operational, and suitable for continued cybersecurity education.

The environment demonstrates practical understanding of virtualization, networking, system administration, and documentation practices.

---

# Next Assessment Targets

Future assessments should include:

* Packet analysis
* Log analysis
* Windows hardening
* Linux hardening
* Authentication review
* Monitoring implementation

---

# Assessment Date

June 2026

# Assessor

Dovud Salimov

# Status

Completed
