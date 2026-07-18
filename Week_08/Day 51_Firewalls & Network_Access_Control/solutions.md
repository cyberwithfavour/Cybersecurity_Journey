# Day 51 – Solutions

## Theory Questions

### Question 1

**What is a firewall, and what is its primary purpose?**

A firewall is a security device or software application that monitors and controls incoming and outgoing network traffic based on predefined security rules.

Its primary purpose is to prevent unauthorized access while allowing legitimate network communication.

---

### Question 2

**Differentiate between a hardware firewall and a software firewall.**

### Hardware Firewall

- Physical security appliance
- Protects an entire network
- Usually deployed at the network perimeter

Examples:
- Cisco ASA
- Fortinet FortiGate
- Palo Alto Firewall

### Software Firewall

- Installed on an individual computer or server
- Protects a single device
- Easier to manage on endpoints

Examples:
- Windows Defender Firewall
- Linux UFW
- macOS Firewall

---

### Question 3

**Explain the difference between a stateless firewall and a stateful firewall.**

### Stateless Firewall

- Inspects each packet independently
- Does not remember previous connections
- Faster but less secure

### Stateful Firewall

- Tracks active network sessions
- Determines whether packets belong to an established connection
- More secure because it understands connection state

---

### Question 4

**What information does a packet-filtering firewall examine before making a decision?**

A packet-filtering firewall examines:

- Source IP Address
- Destination IP Address
- Source Port
- Destination Port
- Protocol (TCP, UDP, ICMP)

It then compares this information against configured firewall rules.

---

### Question 5

**What is a Next-Generation Firewall (NGFW), and how does it differ from a traditional firewall?**

A Next-Generation Firewall (NGFW) combines traditional firewall capabilities with advanced security features such as:

- Intrusion Prevention System (IPS)
- Application awareness
- SSL inspection
- Malware detection
- User identity awareness

Unlike traditional firewalls, NGFWs inspect traffic beyond ports and IP addresses.

---

### Question 6

**What is an Access Control List (ACL)?**

An Access Control List (ACL) is a set of rules that determines whether network traffic is allowed or denied based on criteria such as IP addresses, ports, and protocols.

---

### Question 7

**Explain the difference between inbound traffic and outbound traffic.**

### Inbound Traffic

Traffic entering the organization's network from external sources.

Example:
A user accessing the company's web server.

### Outbound Traffic

Traffic leaving the organization's network to external destinations.

Example:
An employee browsing the internet.

---

### Question 8

**Why is network segmentation important in cybersecurity?**

Network segmentation divides a network into smaller security zones.

Benefits include:

- Reduces lateral movement
- Limits the impact of attacks
- Improves access control
- Protects sensitive systems
- Simplifies security monitoring

---

# Practical Task – Expected Investigation

## Alert Type

Blocked Outbound Connection

---

## Alert Source

Firewall

---

## Source Host

192.168.15.35

---

## Destination IP

185.231.54.20

---

## Destination Port

TCP 443 (HTTPS)

---

## Initial Analysis

The firewall detected an outbound HTTPS connection attempt from an internal workstation to an IP address listed in the organization's threat intelligence feed as malicious.

The firewall successfully blocked the connection before communication could be established.

---

## Possible Explanation

The workstation may have:

- Attempted to contact a malicious command-and-control (C2) server.
- Been infected with malware.
- Accessed a malicious website.
- Triggered a false positive (less likely until verified).

---

## Severity

**High**

### Reason

Although the firewall blocked the connection, an internal device attempted to communicate with a known malicious IP address. This could indicate malware infection or an already compromised endpoint.

---

## Recommended Actions

- Validate the firewall alert.
- Review SIEM logs for related activity.
- Check endpoint security logs.
- Scan the workstation for malware.
- Review DNS and proxy logs.
- Isolate the workstation if additional malicious activity is observed.
- Escalate the incident to Tier 2 SOC.

---

## Investigation Outcome

The firewall successfully prevented communication with a known malicious IP address.

The source workstation requires additional investigation to determine whether it is compromised or whether the alert resulted from legitimate activity.
