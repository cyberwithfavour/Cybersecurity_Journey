# Day 18 – Common Network Attacks

## Objective

Understand common network attacks, how they work, their impact, and the security controls used to defend against them.

---

# What is a Network Attack?

A network attack is an attempt by an attacker to gain unauthorized access to a network, steal information, disrupt services, or compromise systems.

Attackers may target:
- Computers
- Servers
- Routers
- Switches
- Wireless Networks
- Web Applications

---

# Denial-of-Service (DoS) Attack

A Denial-of-Service (DoS) attack attempts to make a system or network unavailable by overwhelming it with excessive traffic.

Imagine 10,000 people trying to enter a small shop at the same time. Genuine customers cannot get in because the entrance is blocked.

Goal:
- Disrupt availability
- Prevent legitimate users from accessing services

---

# Distributed Denial-of-Service (DDoS)

A DDoS attack is similar to a DoS attack, but instead of one computer launching the attack, thousands or even millions of compromised devices attack the target simultaneously.

These infected devices are known as a Botnet.

Examples:
- Mirai Botnet
- IoT device attacks

Why is DDoS more dangerous?
- Harder to stop
- Generates much more traffic
- Often originates from different countries

---

# Man-in-the-Middle (MITM) Attack

A Man-in-the-Middle attack occurs when an attacker secretly intercepts communication between two parties.

Example:

User ↔ Attacker ↔ Website

The attacker can:
- Read sensitive information
- Modify data
- Steal login credentials

Common Targets:
- Public Wi-Fi
- Unencrypted websites

Protection:
- HTTPS
- VPN
- Encryption

---

# Packet Sniffing

Packet sniffing is the process of capturing and analyzing network traffic.

Network administrators use packet sniffers for troubleshooting.

Attackers use them to steal:
- Passwords
- Credit card information
- Sensitive data

Example Tool:
- Wireshark

Protection:
- Encryption
- HTTPS
- VPN

---

# ARP Spoofing

ARP (Address Resolution Protocol) Spoofing occurs when an attacker sends fake ARP messages on a Local Area Network.

Goal:
- Redirect traffic
- Launch a Man-in-the-Middle attack

Protection:
- Dynamic ARP Inspection (DAI)
- Static ARP entries
- Network monitoring

---

# DNS Spoofing

DNS Spoofing (DNS Cache Poisoning) tricks users into visiting fake websites by providing incorrect IP addresses.

Example:

You type:

www.bank.com

Instead of reaching the real bank website, you're redirected to a fake website controlled by an attacker.

Goal:
- Steal usernames
- Steal passwords
- Install malware

Protection:
- DNSSEC
- HTTPS
- Secure DNS servers

---

# Replay Attack

In a Replay Attack, an attacker captures legitimate network traffic and retransmits it later to gain unauthorized access.

Example:
An attacker captures an authentication request and reuses it to impersonate a user.

Protection:
- Nonces
- Timestamps
- Session tokens

---

# Session Hijacking

A Session Hijacking attack occurs when an attacker steals a user's active session.

Instead of stealing the password, the attacker steals the session cookie.

Result:
The attacker gains access without logging in.

Protection:
- HTTPS
- Secure cookies
- Session expiration

---

# Why These Attacks Matter

Understanding attack methods helps security professionals:
- Detect suspicious activity.
- Configure firewalls and IDS/IPS.
- Secure network communication.
- Reduce security risks.

---

# Key Takeaways

- DoS attacks overwhelm one system.
- DDoS attacks overwhelm a system using many compromised devices.
- MITM attacks intercept communication.
- Packet sniffing captures network traffic.
- ARP Spoofing redirects traffic inside a LAN.
- DNS Spoofing redirects users to fake websites.
- Replay attacks reuse captured network traffic.
- Session Hijacking steals active user sessions.
