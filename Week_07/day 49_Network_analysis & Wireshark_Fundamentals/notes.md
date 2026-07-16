# Day 49 Notes – Network Traffic Analysis & Wireshark Fundamentals

# What is Network Traffic?

Network traffic refers to the flow of data between devices over a network.

Whenever you browse the internet, send an email, stream a video, or access a cloud service, data travels across the network in the form of packets.

Monitoring network traffic helps organizations identify normal activity, detect suspicious behavior, and investigate security incidents.

---

# Why is Network Traffic Analysis Important?

Network traffic analysis helps security teams:

- Detect cyber attacks
- Identify malware communication
- Monitor network performance
- Investigate suspicious activities
- Detect data exfiltration
- Respond to security incidents

By analyzing network traffic, SOC analysts can understand how devices communicate and identify unusual patterns.

---

# What is a Packet?

A packet is the smallest unit of data transmitted across a network.

Each packet contains:

- Source IP Address
- Destination IP Address
- Protocol
- Source Port
- Destination Port
- Payload (Actual Data)

Thousands of packets travel across networks every second.

---

# What is Packet Analysis?

Packet analysis is the process of capturing and examining network packets to understand network activity.

SOC analysts perform packet analysis to:

- Investigate attacks
- Troubleshoot network issues
- Detect malicious communication
- Understand attacker behavior

---

# What is Wireshark?

Wireshark is a free and open-source network protocol analyzer.

It captures and displays network packets in real time.

It is one of the most widely used tools by:

- SOC Analysts
- Incident Responders
- Network Engineers
- Digital Forensics Investigators

---

# Common Uses of Wireshark

- Capture network traffic
- Analyze protocols
- Troubleshoot connectivity issues
- Investigate malware traffic
- Detect suspicious communication

---

# Common Network Protocols

## TCP (Transmission Control Protocol)

Reliable communication protocol.

Used by:

- HTTP
- HTTPS
- FTP
- SSH

---

## UDP (User Datagram Protocol)

Faster than TCP but does not guarantee delivery.

Used by:

- DNS
- VoIP
- Streaming services

---

## HTTP (Hypertext Transfer Protocol)

Transfers web pages without encryption.

Default Port:

80

---

## HTTPS (Hypertext Transfer Protocol Secure)

Encrypted version of HTTP.

Default Port:

443

Protects communication between users and websites.

---

## DNS (Domain Name System)

Translates domain names into IP addresses.

Example:

google.com → 142.250.x.x

Default Port:

53

---

## ICMP (Internet Control Message Protocol)

Used for diagnostics.

Example:

Ping

---

## ARP (Address Resolution Protocol)

Maps IP addresses to MAC addresses on a local network.

---

# TCP Three-Way Handshake

Before two devices communicate using TCP, they establish a connection through three steps.

Step 1

Client sends:

SYN

---

Step 2

Server responds:

SYN-ACK

---

Step 3

Client replies:

ACK

Connection established.

This process ensures reliable communication.

---

# DNS Traffic

Every time a user visits a website, a DNS query is generated.

Example:

User enters:

www.google.com

↓

DNS Server returns Google's IP Address

↓

Browser connects to the website.

Attackers often abuse DNS for:

- Malware communication
- Data exfiltration
- Command-and-Control (C2)

---

# HTTP vs HTTPS

HTTP

- Not encrypted
- Less secure
- Port 80

HTTPS

- Encrypted
- More secure
- Port 443

SOC analysts monitor both protocols during investigations.

---

# Indicators of Suspicious Network Activity

Examples include:

- Excessive DNS requests
- Connections to unknown IP addresses
- Large outbound data transfers
- Repeated failed connections
- Communication with malicious domains
- Unusual traffic outside business hours

---

# Key Takeaways

- Network traffic consists of packets exchanged between devices.
- Wireshark captures and analyzes network traffic.
- TCP provides reliable communication using the three-way handshake.
- DNS translates domain names into IP addresses.
- HTTPS encrypts web traffic while HTTP does not.
- Abnormal network traffic may indicate malicious activity.
- Packet analysis is a fundamental skill for SOC analysts.
