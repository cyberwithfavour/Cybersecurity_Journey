# Day 14 – Common Network Ports & Protocols

## Objective

Learn the most common network protocols, their default port numbers, and their role in secure communication.

---

# What is a Port?

A port is a logical communication endpoint that allows applications and services to send and receive data over a network.

Think of an IP address as the address of a house, while a port is the specific room inside that house.

One device can have many open ports, each used by a different application.

Example:

IP Address:
192.168.1.20

Port:
443 (HTTPS)

Together:
192.168.1.20:443

---

# What is a Protocol?

A protocol is a set of rules that devices follow when communicating over a network.

Protocols define:
- How data is sent.
- How data is received.
- How errors are handled.
- How devices understand each other.

---

# Common Network Protocols

## HTTP

Hypertext Transfer Protocol

Purpose:
Transfers web pages over the Internet.

Port:
80

Security:
Not encrypted.

Example:
http://example.com

---

## HTTPS

Hypertext Transfer Protocol Secure

Purpose:
Secure web communication.

Port:
443

Security:
Encrypted using SSL/TLS.

Example:
https://example.com

---

## FTP

File Transfer Protocol

Purpose:
Transfers files between computers.

Port:
21

Security:
Not encrypted.

---

## SFTP

SSH File Transfer Protocol

Purpose:
Securely transfers files.

Port:
22

Security:
Encrypted using SSH.

---

## SSH

Secure Shell

Purpose:
Secure remote administration of systems.

Port:
22

Example:
Managing a Linux server remotely.

---

## Telnet

Purpose:
Remote access to devices.

Port:
23

Security:
Not encrypted.

Because it sends usernames and passwords in plain text, Telnet is considered insecure and has largely been replaced by SSH.

---

## DNS

Domain Name System

Purpose:
Converts domain names into IP addresses.

Port:
53

Example:

www.google.com

↓

142.250.x.x

---

## DHCP

Dynamic Host Configuration Protocol

Purpose:
Automatically assigns IP addresses to devices.

Ports:
67 (Server)
68 (Client)

Without DHCP, devices would need manual IP configuration.

---

## SMTP

Simple Mail Transfer Protocol

Purpose:
Sends email.

Port:
25

---

## POP3

Post Office Protocol Version 3

Purpose:
Downloads email to a local device.

Port:
110

---

## IMAP

Internet Message Access Protocol

Purpose:
Allows users to read email while keeping messages on the server.

Port:
143

---

## RDP

Remote Desktop Protocol

Purpose:
Allows remote access to Windows computers.

Port:
3389

---

## LDAP

Lightweight Directory Access Protocol

Purpose:
Accesses directory services like Microsoft Active Directory.

Port:
389

---

# Secure vs Insecure Protocols

| Secure | Insecure |
|---------|----------|
| HTTPS | HTTP |
| SSH | Telnet |
| SFTP | FTP |

Always choose encrypted protocols whenever possible.

---

# Why Ports Matter in Cybersecurity

Attackers often scan ports to identify running services.

Examples:
- Open SSH port may be targeted with brute-force attacks.
- Open RDP port can be exploited if not secured.
- Open HTTP traffic can be intercepted because it is not encrypted.

Security professionals monitor open ports and close unnecessary ones to reduce the attack surface.

---

# Common Security Best Practices

- Disable unused services.
- Close unnecessary ports.
- Replace insecure protocols with secure alternatives.
- Use firewalls to control network traffic.
- Keep services updated with security patches.

---

# Key Takeaways

- Ports identify specific services on a device.
- Protocols define communication rules.
- HTTPS is more secure than HTTP.
- SSH replaces Telnet.
- SFTP replaces FTP.
- DNS translates domain names into IP addresses.
- DHCP automatically assigns IP addresses.
- Open ports can become attack vectors if not secured.
