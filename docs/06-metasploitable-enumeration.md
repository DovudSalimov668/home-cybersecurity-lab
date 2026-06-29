# Metasploitable 2 Enumeration Assessment

## Purpose

This document records the initial enumeration of the Metasploitable 2 virtual machine.

The objective is to identify exposed services and understand attack surface visibility through standard reconnaissance techniques.

No exploitation activities are documented in this report.

---

# Target Information

## Hostname

metasploitable

## Operating System

Ubuntu-based legacy Linux system

## IP Address

192.168.248.132

## Network

Host-Only only

## Internet Access

Disabled

---

# Discovery Methodology

## Host Discovery

Tool:

Nmap

Purpose:

Identify active hosts on the Host-Only network.

---

## Service Enumeration

Tool:

Nmap Service Detection

Command:

```bash
nmap -sV 192.168.248.132
```

Purpose:

Identify running services and software versions.

---

# Enumeration Results

## FTP

Port:

21/TCP

Detected Service:

vsftpd 2.3.4

Risk Level:

High

Reason:

Legacy FTP service with known historical security concerns.

---

## SSH

Port:

22/TCP

Detected Service:

OpenSSH 4.7p1

Risk Level:

Medium

Reason:

Remote administration service.

---

## Telnet

Port:

23/TCP

Risk Level:

High

Reason:

Credentials transmitted without encryption.

---

## SMTP

Port:

25/TCP

Detected Service:

Postfix

Risk Level:

Medium

Reason:

Mail services require careful configuration.

---

## DNS

Port:

53/TCP

Detected Service:

BIND 9.4.2

Risk Level:

Medium

---

## HTTP

Port:

80/TCP

Detected Service:

Apache 2.2.8

Risk Level:

Medium

---

## Samba

Ports:

139/TCP

445/TCP

Risk Level:

High

Reason:

File sharing services increase exposure.

---

## NFS

Port:

2049/TCP

Risk Level:

Medium

---

## MySQL

Port:

3306/TCP

Risk Level:

High

Reason:

Database exposure.

---

## PostgreSQL

Port:

5432/TCP

Risk Level:

High

Reason:

Database exposure.

---

## VNC

Port:

5900/TCP

Risk Level:

Medium

---

## IRC

Port:

6667/TCP

Detected Service:

UnrealIRCd

Risk Level:

High

---

## Tomcat

Port:

8180/TCP

Risk Level:

Medium

---

# Attack Surface Analysis

Observed Characteristics:

* Large number of exposed services
* Legacy software versions
* Multiple remote administration protocols
* Database exposure
* Web application exposure
* File sharing exposure

---

# Security Observations

Modern production servers rarely expose this many services simultaneously.

The machine intentionally demonstrates poor security practices for educational purposes.

---

# Learning Outcomes

This target allows practice in:

* Host discovery
* Port scanning
* Service identification
* Version detection
* Risk prioritization
* Technical documentation

---

# Conclusion

Metasploitable 2 presents a large and intentionally insecure attack surface suitable for controlled security training within an isolated environment.
