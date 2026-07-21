# Day 57 – Notes

## Secure Network Architecture

Secure Network Architecture is the process of designing a network in a way that protects an organization's systems, users, and data from cyber threats while allowing legitimate business operations to continue efficiently.

A well-designed network does not rely on a single security device. Instead, it uses multiple layers of protection so that if one control fails, others continue protecting the environment.

---

## Why Secure Network Architecture Matters

Organizations depend on their networks to:

- Share data
- Access applications
- Communicate internally and externally
- Connect to cloud services
- Support remote work

Poor network design can lead to:

- Unauthorized access
- Malware spreading quickly
- Data breaches
- Service disruption
- Difficulty detecting attacks

A secure architecture reduces these risks.

---

# Defense in Depth

Defense in Depth is a cybersecurity strategy that uses multiple layers of security controls instead of relying on a single solution.

If one security control is bypassed, additional layers continue protecting the organization.

Examples of security layers include:

- Physical Security
- Network Security
- Endpoint Security
- Identity Security
- Application Security
- Data Security
- Monitoring and Logging
- Incident Response

Think of it like protecting a house:

- Fence
- Gate
- Security cameras
- Alarm system
- Locked doors

Breaking through one layer doesn't provide complete access.

---

# Network Zones

Enterprise networks are divided into security zones.

Each zone has different trust levels.

## External Network

This is the public Internet.

Characteristics:

- Completely untrusted
- Anyone can connect
- Highest risk

Examples:

- Public websites
- External users
- Customers

---

## Internal Network

This contains the organization's trusted resources.

Examples:

- Employee computers
- Internal servers
- File shares
- Printers

Access is usually limited to authorized employees.

---

## DMZ (Demilitarized Zone)

A DMZ is a network placed between the Internet and the internal network.

Its purpose is to expose public services without exposing the internal network.

Common systems placed inside a DMZ include:

- Web Servers
- Email Servers
- DNS Servers
- Reverse Proxies

If an attacker compromises a web server in the DMZ, they should still not have direct access to the internal network.

---

# Trust Boundaries

A trust boundary is a point where the level of trust changes between systems or networks.

Examples include:

- Internet → Firewall
- Firewall → DMZ
- DMZ → Internal Network
- Internal Network → Secure Server Network

Every trust boundary should have security controls that inspect and restrict traffic.

---

# Principle of Least Privilege

Users, devices, and applications should receive only the minimum permissions necessary to perform their jobs.

Benefits:

- Reduces attack surface.
- Limits damage if an account is compromised.
- Prevents unauthorized access.

---

# Network Isolation

Sensitive systems should be isolated from less secure systems.

Examples:

- Finance network
- HR network
- Production servers
- Guest Wi-Fi

Isolation limits attacker movement if one part of the network is compromised.

---

# Secure Communication

Organizations should protect data while it travels across networks.

Common secure protocols include:

- HTTPS
- SSH
- SFTP
- TLS
- IPsec

Avoid insecure protocols such as:

- HTTP
- FTP
- Telnet

---

# Redundancy

Critical network components should have backups.

Examples:

- Backup Firewalls
- Redundant Routers
- Multiple Internet Connections
- Backup DNS Servers

Redundancy improves availability and supports business continuity.

---

# Monitoring

A secure architecture continuously monitors network activity.

Common monitoring solutions include:

- Firewalls
- IDS
- IPS
- SIEM
- Network Monitoring Systems

Monitoring allows security teams to detect attacks early.

---

# Characteristics of a Secure Enterprise Network

A secure enterprise network should be:

- Layered
- Segmented
- Monitored
- Resilient
- Scalable
- Highly Available
- Secure by Design

---

# Why This Matters to a SOC Analyst

SOC analysts protect organizations by monitoring enterprise networks.

Understanding how networks are designed helps analysts:

- Identify abnormal traffic.
- Understand where attacks originate.
- Trace attacker movement.
- Recommend containment strategies.
- Investigate incidents more effectively.

A strong understanding of secure network architecture makes it much easier to analyze alerts and understand the impact of a security incident.
