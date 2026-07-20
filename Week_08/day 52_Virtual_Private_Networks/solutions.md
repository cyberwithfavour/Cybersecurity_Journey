# Day 52 – Solutions

## Task 1

### Virtual Private Network (VPN)

A VPN is a technology that creates a secure, encrypted connection between a user's device and a private network over the Internet.

---

### VPN Tunnel

A VPN tunnel is the encrypted pathway through which data travels securely between a user's device and the VPN server.

---

### Remote Access VPN

A Remote Access VPN allows individual users to securely connect to an organization's internal network from a remote location.

---

### Site-to-Site VPN

A Site-to-Site VPN securely connects two or more office networks over the Internet.

---

### Full Tunnel VPN

A Full Tunnel VPN sends all network traffic through the encrypted VPN tunnel.

---

### Split Tunnel VPN

A Split Tunnel VPN sends only company-related traffic through the VPN while regular Internet traffic uses the local network.

---

## Task 2

| Feature | Remote Access VPN | Site-to-Site VPN |
|----------|-------------------|------------------|
| Purpose | Secure remote user access | Connect multiple office networks |
| Users | Individual employees | Entire office locations |
| Example | Employee working from home | Lagos office connected to Abuja office |

---

## Task 3

### IPsec

Provides secure communication by encrypting IP traffic between devices.

### SSL/TLS

Uses web-based encryption to provide secure remote access through browsers or VPN clients.

### OpenVPN

An open-source VPN protocol known for its strong security and flexibility.

### WireGuard

A modern VPN protocol designed to be fast, lightweight, and highly secure.

---

## Task 4

### 1. Why is encryption important in a VPN connection?

Encryption protects data from being intercepted or read while it travels across the Internet.

---

### 2. Why should Multi-Factor Authentication (MFA) be enabled?

MFA adds an extra layer of security, making it more difficult for attackers to access VPN accounts even if passwords are stolen.

---

### 3. Two risks if a VPN account is compromised

- Unauthorized access to the company's internal network.
- Data theft or further compromise of internal systems.

---

## Task 5

### Is this activity suspicious?

Yes.

---

### What type of alert could this generate?

Impossible Travel Alert.

---

### What evidence would you collect?

- VPN login logs
- Source IP addresses
- Geolocation information
- Authentication logs
- Device information
- User activity logs

---

### Would you escalate the incident?

Yes.

A successful login from two geographically distant locations within a short period may indicate credential compromise and requires immediate investigation.

---

## Practical Exercise

### Cisco AnyConnect

- Primary Use: Enterprise remote access
- Authentication: Username/Password, MFA, Certificates
- Environment: Large organizations

---

### Palo Alto GlobalProtect

- Primary Use: Secure remote workforce access
- Authentication: MFA, Certificates, SSO
- Environment: Enterprise networks

---

### OpenVPN

- Primary Use: Secure remote connections
- Authentication: Certificates, Username/Password
- Environment: Small businesses, enterprises, and personal use
