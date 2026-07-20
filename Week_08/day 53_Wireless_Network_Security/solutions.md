# Day 53 – Solutions

## Task 1

### Wireless Network Security

Wireless Network Security refers to the measures used to protect Wi-Fi networks from unauthorized access, attacks, and data theft.

---

### WEP

WEP (Wired Equivalent Privacy) is the first wireless security protocol. It uses weak encryption and is no longer considered secure.

---

### WPA2

WPA2 (Wi-Fi Protected Access 2) is a wireless security standard that uses AES encryption to provide strong protection for Wi-Fi networks.

---

### WPA3

WPA3 (Wi-Fi Protected Access 3) is the latest wireless security standard, offering stronger encryption and improved protection against password attacks.

---

### Rogue Access Point

A Rogue Access Point is an unauthorized wireless access point connected to a network without approval.

---

### Evil Twin Attack

An Evil Twin Attack occurs when an attacker creates a fake Wi-Fi network that appears to be legitimate in order to steal user information.

---

### Deauthentication Attack

A Deauthentication Attack forces users to disconnect from a wireless network by sending fake deauthentication frames.

---

## Task 2

| Wireless Standard | Encryption | Security Level | Recommended? |
|-------------------|------------|----------------|--------------|
| WEP | RC4 | Low | ❌ No |
| WPA | TKIP | Medium | ❌ No |
| WPA2 | AES | High | ✅ Yes |
| WPA3 | AES (SAE Authentication) | Very High | ✅ Yes |

---

## Task 3

### 1. Why is WEP no longer considered secure?

WEP uses weak encryption that can be cracked within minutes using readily available tools.

---

### 2. What makes WPA3 more secure than WPA2?

WPA3 provides stronger authentication, better encryption, and increased protection against password guessing and brute-force attacks.

---

### 3. Why should organizations regularly monitor their wireless networks?

To detect unauthorized devices, rogue access points, suspicious wireless activity, and potential attacks before they impact the organization.

---

## Task 4

### What could this indicate?

The presence of a Rogue Access Point or an unauthorized device connected to the network.

---

### What evidence would you collect?

- Wireless controller logs
- Device MAC address
- IP address
- SSID information
- Connected clients
- Authentication logs

---

### What risks does a rogue access point introduce?

- Unauthorized network access
- Data interception
- Credential theft
- Malware distribution
- Network compromise

---

### What would be your first response?

Identify the device, verify whether it is authorized, isolate it from the network if necessary, and escalate the incident according to the organization's incident response procedures.

---

## Task 5

### Rogue Access Point

An unauthorized wireless device connected to a corporate network.

### Evil Twin Attack

A fake Wi-Fi network designed to trick users into connecting and revealing sensitive information.

### Deauthentication Attack

An attack that disconnects users from a Wi-Fi network to disrupt service or capture authentication handshakes.

### Password Brute Force Attack

An attack where an attacker repeatedly tries different passwords until the correct Wi-Fi password is found.

---

## Practical Exercise

### Cisco Wireless LAN Controller (WLC)

- Primary Use: Centralized wireless network management
- Security Features: WPA3, 802.1X, Rogue AP Detection
- Typical Environment: Enterprise

---

### Aruba Wireless

- Primary Use: Enterprise wireless networking
- Security Features: Dynamic Segmentation, WPA3, IDS/IPS
- Typical Environment: Enterprise and Campus

---

### Ubiquiti UniFi

- Primary Use: Wireless network management
- Security Features: WPA3, Guest Isolation, Device Monitoring
- Typical Environment: Small Business and Enterprise
