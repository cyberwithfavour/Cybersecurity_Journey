# Day 49 – Solutions

## Task 1

### What is network traffic, and why is it important for cybersecurity?

Network traffic refers to the flow of data between devices across a network. Every activity such as browsing the internet, sending emails, streaming videos, or accessing cloud services generates network traffic.

It is important because it helps security teams detect cyber attacks, investigate suspicious activities, identify malware communication, monitor network performance, and prevent data exfiltration.

---

## Task 2

### What is a packet?

A packet is the smallest unit of data transmitted across a network.

A packet can contain:

- Source IP Address
- Destination IP Address
- Source Port
- Destination Port
- Protocol
- Payload (Actual Data)

---

## Task 3

### Explain the purpose of packet analysis.

Packet analysis is the process of capturing and examining network packets to understand how devices communicate.

SOC analysts use packet analysis to:

- Investigate security incidents
- Detect malicious traffic
- Troubleshoot network issues
- Identify attacker communication
- Analyze network behavior

---

## Task 4

### What is Wireshark, and why is it commonly used by SOC analysts?

Wireshark is a free and open-source network protocol analyzer.

It allows analysts to capture and inspect network packets in real time.

SOC analysts use Wireshark to:

- Analyze network traffic
- Investigate suspicious connections
- Detect malware communication
- Troubleshoot network problems
- Perform forensic investigations

---

## Task 5

### Differentiate between the following protocols.

### TCP

Reliable connection-oriented protocol that guarantees data delivery.

---

### UDP

Connectionless protocol that is faster than TCP but does not guarantee delivery.

---

### HTTP

Transfers web pages without encryption.

Default Port: 80

---

### HTTPS

Encrypted version of HTTP that protects communication between users and websites.

Default Port: 443

---

### DNS

Translates domain names into IP addresses.

Default Port: 53

---

## Task 6

### Explain the TCP Three-Way Handshake.

The TCP Three-Way Handshake establishes a reliable connection between two devices.

Step 1:
Client sends **SYN**.

Step 2:
Server responds with **SYN-ACK**.

Step 3:
Client replies with **ACK**.

Once these three steps are completed, communication begins.

---

## Task 7

### Why is DNS important? How can attackers abuse DNS?

DNS translates human-readable domain names into IP addresses so computers can locate websites and services.

Attackers may abuse DNS by:

- Communicating with malware (Command-and-Control)
- Data exfiltration
- DNS tunneling
- Connecting infected devices to malicious domains

---

## Task 8

### List at least five indicators of suspicious network activity.

Examples include:

- Excessive DNS requests
- Connections to unknown IP addresses
- Large outbound data transfers
- Repeated failed connections
- Communication with malicious domains
- Unusual traffic outside business hours

---

# Practical Task

## Status

✅ Completed

The hands-on investigation for today's lesson has been documented separately in my **SOC-Labs** repository.

**Repository:** SOC-Labs

**Project:** Investigation_004_Suspicious_DNS_Traffic

This investigation includes alert validation, evidence collection, DNS traffic analysis, severity assessment, recommendations, and lessons learned.
