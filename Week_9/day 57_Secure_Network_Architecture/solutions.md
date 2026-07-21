# Day 57 – Solutions

## Task 1

### Secure Network Architecture

The design of a network that incorporates security controls, segmentation, monitoring, and secure communication to protect systems, users, and data from cyber threats.

---

### Defense in Depth

A security strategy that uses multiple layers of security controls so that if one layer fails, additional layers continue to provide protection.

---

### DMZ (Demilitarized Zone)

A separate network that hosts public-facing services, allowing external users to access them without exposing the internal network.

---

### Trust Boundary

A point where data moves between networks or systems with different levels of trust, requiring security controls to inspect and regulate traffic.

---

### Network Isolation

The practice of separating sensitive systems or networks to reduce the spread of attacks and limit unauthorized access.

---

### Redundancy

The use of backup systems or components to ensure services remain available if a primary component fails.

---

### Least Privilege

A security principle where users, devices, and applications receive only the minimum permissions necessary to perform their tasks.

---

### Secure Communication

The use of encrypted protocols to protect data while it is transmitted across networks.

---

## Task 2

| Concept | Purpose |
|---------|---------|
| Defense in Depth | Provides multiple layers of protection against attacks. |
| DMZ | Hosts public-facing services while protecting the internal network. |
| Internal Network | Stores trusted organizational resources and systems. |
| External Network | Represents the public Internet where users and attackers originate. |
| Trust Boundary | Controls and monitors traffic moving between different security zones. |
| Network Isolation | Prevents attackers from moving freely between systems. |
| Redundancy | Maintains availability during failures. |
| Secure Communication | Protects data from interception through encryption. |

---

## Task 3

### 1. Why is Defense in Depth more effective than relying on a single security control?

Because no single security control is perfect. Multiple layers reduce the likelihood that an attacker can compromise the entire environment if one defense is bypassed.

---

### 2. Why shouldn't public-facing servers be placed directly inside the internal network?

Because if they are compromised, attackers could gain direct access to sensitive internal systems, increasing the risk of data breaches and lateral movement.

---

### 3. What is the purpose of a DMZ in an enterprise network?

To safely host public-facing services while separating them from the organization's trusted internal network.

---

### 4. How does network segmentation reduce the impact of a cyberattack?

It limits an attacker's ability to move between systems, containing the attack to a smaller portion of the network.

---

### 5. Why are trust boundaries important in enterprise security?

They identify where different levels of trust meet, allowing organizations to inspect, filter, and control traffic between security zones.

---

## Task 4

### Five Security Design Mistakes

- No DMZ for public-facing servers.
- Public website is located inside the internal network.
- Email server is not isolated.
- DNS server is directly exposed from the internal network.
- No network segmentation between critical systems.

---

### Systems at Risk

- Employee workstations
- File server
- Email server
- DNS server
- Any other systems connected to the internal network

---

### Possible Attacker Movement

After compromising the web server, the attacker could:

- Scan the internal network.
- Move laterally to employee devices.
- Attempt to steal credentials.
- Access the file server.
- Target other internal services.

---

### Security Principles Ignored

- Defense in Depth
- Network Segmentation
- Network Isolation
- Trust Boundaries
- Least Privilege

---

### Improved Architecture

```
Internet
      │
Firewall
      │
     DMZ
 ┌──────────────┐
 │ Web Server   │
 │ Email Server │
 │ DNS Server   │
 └──────────────┘
      │
Internal Firewall
      │
Internal Network
 ┌──────────────┐
 │ Employee PCs │
 │ File Server  │
 │ Database     │
 └──────────────┘
```

This design ensures that even if a public-facing server is compromised, attackers must still bypass another security layer before reaching internal systems.

---

## Task 5

### HTTPS

**Primary Purpose**

Secure web browsing.

**Default Port**

443

**Why Secure**

Uses TLS encryption to protect web traffic.

---

### SSH

**Primary Purpose**

Secure remote administration.

**Default Port**

22

**Why Secure**

Encrypts remote login sessions and command execution.

---

### SFTP

**Primary Purpose**

Secure file transfer.

**Default Port**

22

**Why Secure**

Uses SSH encryption to protect file transfers.

---

### TLS

**Primary Purpose**

Encrypt communication between applications.

**Default Port**

Varies depending on the application.

**Why Secure**

Provides encryption, integrity, and authentication.

---

### IPsec

**Primary Purpose**

Secure network communication, commonly used with VPNs.

**Default Port**

Uses ESP (Protocol 50), AH (Protocol 51), and IKE over UDP 500/4500.

**Why Secure**

Encrypts IP packets and authenticates communicating devices.

---

## Practical Exercise

### Trust Boundaries

- Internet ↔ Firewall
- Firewall ↔ DMZ
- DMZ ↔ Internal Firewall
- Internal Firewall ↔ Internal Network

---

### Systems That Should Never Be Directly Exposed

- Database Server
- File Server
- Employee Workstations
- Domain Controllers
- Backup Servers

---

### Security Controls After Web Server Compromise

- Firewall rules
- Internal firewall between DMZ and internal network
- Network segmentation
- IDS/IPS monitoring
- SIEM alerting
- Access control policies
- Endpoint Detection & Response (EDR)

These controls help contain the attack and prevent the attacker from reaching critical internal systems.
