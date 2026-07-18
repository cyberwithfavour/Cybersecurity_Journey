# Day 51 – Firewalls & Network Access Control

## What is a Firewall?

A firewall is a network security device or software application that monitors and controls incoming and outgoing network traffic based on predefined security rules.

Its primary purpose is to prevent unauthorized access while allowing legitimate communication.

Think of a firewall as a security checkpoint. Every packet must pass through it before entering or leaving the network.

---

## Why Organizations Use Firewalls

Firewalls help organizations:

- Prevent unauthorized access
- Block malicious traffic
- Enforce security policies
- Protect internal systems
- Reduce attack surfaces
- Control network communication

---

## Types of Firewalls

### Hardware Firewall

A physical device placed between networks.

Examples:

- Cisco ASA
- Fortinet FortiGate
- Palo Alto Networks Firewall

Advantages

- Protects the entire network
- High performance
- Enterprise security

---

### Software Firewall

Installed directly on a computer or server.

Examples

- Windows Defender Firewall
- Linux UFW
- macOS Firewall

Advantages

- Protects individual devices
- Easy to configure
- Suitable for personal computers

---

## Packet Filtering Firewall

Examines packets using information such as:

- Source IP
- Destination IP
- Source Port
- Destination Port
- Protocol

The firewall either allows or blocks traffic based on predefined rules.

---

## Stateless Firewall

Makes decisions based only on individual packets.

It does not remember previous connections.

Advantages

- Fast
- Simple

Disadvantages

- Less secure

---

## Stateful Firewall

Tracks active network connections.

The firewall understands whether packets belong to an established session.

Advantages

- More secure
- Better at preventing unauthorized connections

---

## Next-Generation Firewall (NGFW)

An NGFW provides traditional firewall functionality plus additional security features.

Common capabilities include:

- Application awareness
- Intrusion Prevention System (IPS)
- Malware detection
- SSL inspection
- User identity awareness

Examples

- Palo Alto
- Fortinet
- Cisco Firepower

---

## Access Control Lists (ACLs)

ACLs define which traffic is permitted or denied.

Example

Allow:

- HTTPS (443)
- DNS (53)

Deny:

- Telnet (23)

---

## Inbound vs Outbound Traffic

### Inbound

Traffic entering the internal network.

Firewalls inspect incoming traffic to prevent attacks.

---

### Outbound

Traffic leaving the internal network.

Organizations also monitor outbound traffic because malware often communicates with external servers.

---

## Network Segmentation

Firewalls help separate networks into security zones.

Examples

- Users
- Servers
- Guest Wi-Fi
- Data Center

Segmentation limits attacker movement if one system is compromised.

---

## Firewalls in a SOC

Typical workflow

1. Firewall blocks or logs suspicious traffic.
2. Logs are forwarded to the SIEM.
3. SIEM correlates firewall events with other logs.
4. Tier 1 analyst validates alerts.
5. Investigation begins if necessary.

---

## Key Terms

- Firewall
- Packet Filtering
- Stateful Inspection
- Stateless Inspection
- NGFW
- ACL
- Network Segmentation
- Inbound Traffic
- Outbound Traffic
