# Network Architecture Documentation

## Purpose

This document describes the network architecture used in the Home Cybersecurity Lab.

The design separates internet access from internal training traffic while allowing controlled communication between virtual machines.

---

# Network Overview

The environment consists of two logical networks:

1. Host-Only Network
2. NAT Network

This architecture provides:

* Internal isolation
* Internet access where required
* Safe training environment
* Controlled attack surface

---

# Network Diagram

```text
                          INTERNET
                              |
                              |
                       VMware NAT
                       192.168.198.0/24
                              |
         -------------------------------------------------
         |                       |                       |
         |                       |                       |
      Ubuntu                 Kali Linux             Windows 11
   192.168.198.132       192.168.198.133        192.168.198.134
         |                       |                       |
         -------------------------------------------------
                              |
                              |
                     Host-Only Network
                     192.168.248.0/24
                              |
 ---------------------------------------------------------------
 |                  |                    |                     |
 |                  |                    |                     |
Ubuntu           Kali Linux         Windows 11        Metasploitable 2
248.130          248.131            248.128           248.132
```

---

# Host-Only Network

## Subnet

192.168.248.0/24

## Purpose

Used for:

* Enumeration
* Packet captures
* SSH communication
* Service discovery
* Internal testing

## Hosts

| System           | Address         |
| ---------------- | --------------- |
| Windows 11       | 192.168.248.128 |
| Ubuntu Server    | 192.168.248.130 |
| Kali Linux       | 192.168.248.131 |
| Metasploitable 2 | 192.168.248.132 |

---

# NAT Network

## Subnet

192.168.198.0/24

## Purpose

Used for:

* Internet access
* Software installation
* System updates
* Package downloads

## Hosts

| System        | Address         |
| ------------- | --------------- |
| Ubuntu Server | 192.168.198.132 |
| Kali Linux    | 192.168.198.133 |
| Windows 11    | 192.168.198.134 |

---

# Routing Analysis

## Kali Linux

Default Route:

192.168.198.2

Interface:

eth1

Purpose:

Internet connectivity

---

## Ubuntu Server

Default Route:

192.168.198.2

Interface:

ens37

Purpose:

Internet connectivity

---

## Windows 11

Default Gateway:

192.168.198.2

Interface:

Ethernet1

Purpose:

Internet connectivity

---

# Security Decisions

## Decision 1

Metasploitable 2 has no NAT connectivity.

Reason:

The machine intentionally contains vulnerable services and should not have direct internet access.

---

## Decision 2

Host-Only network used for testing.

Reason:

Prevents accidental interaction with external systems.

---

## Decision 3

Dual-homed administration systems.

Reason:

Allows internet access while maintaining lab communication.

---

# Network Validation

Verified:

* SSH connectivity
* DHCP assignment
* Routing functionality
* Host-Only communication
* Internet connectivity

---

# Future Improvements

* Add pfSense firewall
* Create separate DMZ network
* Add logging network
* Implement VLAN simulation
* Deploy monitoring stack
* Add Active Directory environment
