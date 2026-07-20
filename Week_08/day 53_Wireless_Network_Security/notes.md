# Day 53 – Notes

## What is Wireless Network Security?

Wireless Network Security refers to the measures used to protect wireless networks (Wi-Fi) from unauthorized access, attacks, and data theft.

Since wireless signals travel through the air, anyone within range can potentially attempt to access the network if it is not properly secured.

---

## Why is Wireless Security Important?

Wireless security helps to:

- Prevent unauthorized access.
- Protect sensitive data.
- Maintain confidentiality and integrity.
- Prevent attackers from intercepting network traffic.
- Reduce the risk of network compromise.

---

## Wireless Security Standards

### WEP (Wired Equivalent Privacy)

- First wireless security standard.
- Uses weak encryption.
- Easily cracked.
- **Not recommended.**

---

### WPA (Wi-Fi Protected Access)

- Improved security over WEP.
- Introduced TKIP encryption.
- Better than WEP but now outdated.

---

### WPA2 (Wi-Fi Protected Access 2)

- Uses AES encryption.
- Most widely used wireless security standard.
- Stronger and more secure than WPA.

---

### WPA3 (Wi-Fi Protected Access 3)

- Latest wireless security standard.
- Provides stronger encryption.
- Better protection against password guessing attacks.
- Improved authentication.

---

## Wireless Authentication

Wireless authentication verifies that only authorized users can connect to a wireless network.

Common methods include:

- Pre-Shared Key (PSK)
- Enterprise Authentication (802.1X)
- Multi-Factor Authentication (MFA)

---

## Common Wireless Attacks

### Rogue Access Point

An unauthorized wireless access point connected to a network.

---

### Evil Twin Attack

An attacker creates a fake Wi-Fi network that looks identical to a legitimate one to trick users into connecting.

---

### Deauthentication Attack

An attacker forces devices to disconnect from a wireless network, often to capture authentication handshakes or cause denial of service.

---

### Password Brute Force Attack

Attackers repeatedly try different passwords until they successfully connect to the wireless network.

---

## Wireless Security Best Practices

- Use WPA3 whenever possible.
- Use strong, unique Wi-Fi passwords.
- Enable Multi-Factor Authentication where applicable.
- Disable unused wireless services.
- Regularly update firmware.
- Monitor wireless logs.
- Detect and remove rogue access points.

---

## Wireless Security in a SOC Environment

SOC analysts monitor wireless networks for:

- Rogue Access Points.
- Unauthorized devices.
- Multiple failed authentication attempts.
- Suspicious wireless connections.
- Deauthentication attacks.
- Brute-force attacks.
- Unusual network activity.

Wireless monitoring helps identify threats before they impact the organization's network.
