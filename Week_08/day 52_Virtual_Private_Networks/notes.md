# Day 52 – Notes

## What is a VPN?

A **Virtual Private Network (VPN)** is a technology that creates a secure, encrypted connection between a user's device and a private network over the Internet.

Instead of sending data openly across the Internet, a VPN encrypts the traffic, making it difficult for attackers to intercept or read the information.

---

## Why Do Organizations Use VPNs?

Organizations use VPNs to:

- Allow employees to work remotely.
- Secure communication over public networks.
- Protect sensitive business data.
- Connect branch offices securely.
- Reduce the risk of data interception.

---

## Types of VPN

### Remote Access VPN

A **Remote Access VPN** allows individual users to securely connect to an organization's internal network from anywhere.

**Example:**
An employee working from home securely connects to the company's network.

---

### Site-to-Site VPN

A **Site-to-Site VPN** securely connects two or more office networks over the Internet.

**Example:**
A company's Lagos office connects securely to its Abuja office.

---

## VPN Tunneling

A **VPN tunnel** is the encrypted pathway through which data travels between a user's device and the VPN server.

The tunnel protects data from being viewed or modified while it is transmitted across the Internet.

---

## VPN Authentication

Before a VPN connection is established, the user must prove their identity.

Common authentication methods include:

- Username and Password
- Multi-Factor Authentication (MFA)
- Digital Certificates
- Security Tokens

---

## Full Tunnel vs Split Tunnel

### Full Tunnel

All network traffic passes through the VPN before reaching its destination.

**Advantages**
- Higher security
- Better monitoring
- Improved visibility

---

### Split Tunnel

Only company-related traffic passes through the VPN, while regular Internet traffic uses the local Internet connection.

**Advantages**
- Faster Internet performance
- Reduced bandwidth usage

**Disadvantages**
- Less visibility
- Higher security risk

---

## Common VPN Protocols

Some of the most common VPN protocols include:

- IPsec
- SSL/TLS
- OpenVPN
- WireGuard
- L2TP/IPsec
- IKEv2/IPsec

Each protocol provides secure communication but differs in performance, compatibility, and security features.

---

## VPN Logs

VPN logs may contain information such as:

- Username
- Source IP Address
- Login Time
- Logout Time
- Device Information
- Authentication Status
- Session Duration

These logs are valuable during security investigations because they help analysts determine who accessed the network, when they connected, and from where.

---

## VPN Security Risks

Common VPN-related threats include:

- Stolen credentials
- Brute-force attacks
- Credential stuffing
- Unauthorized remote access
- Compromised endpoints
- Impossible travel
- VPN misconfiguration

---

## VPN in a SOC Environment

SOC Analysts monitor VPN activity to detect suspicious behavior such as:

- Multiple failed login attempts
- Successful logins from unusual countries
- Impossible travel alerts
- Logins outside business hours
- Simultaneous logins from different locations
- Unauthorized VPN access

Investigating these events helps identify compromised accounts and potential security incidents.
