# Day 59 – Notes

# Network Access Control (NAC)

Network Access Control (NAC) is a security solution that controls which users and devices are allowed to connect to a network.

Instead of allowing every device to connect automatically, NAC verifies that both the **user** and the **device** meet the organization's security requirements before granting access.

NAC follows the principle of **"Never trust, always verify."**

---

# Why NAC is Important

Modern organizations have many devices connecting to their networks:

- Employee laptops
- Personal devices (BYOD)
- Smartphones
- Printers
- IoT devices
- Contractor devices
- Guest devices

Without proper access control, an infected or unauthorized device could introduce malware or provide attackers with access to the network.

NAC helps reduce this risk by ensuring only trusted users and compliant devices are allowed to connect.

---

# Objectives of NAC

A Network Access Control solution aims to:

- Authenticate users
- Authenticate devices
- Verify device health
- Enforce security policies
- Restrict unauthorized access
- Monitor connected devices

---

# How NAC Works

A typical NAC process follows these steps:

1. A device attempts to connect to the network.
2. The NAC solution authenticates the user.
3. The device is checked for compliance.
4. Security policies are evaluated.
5. Appropriate network access is granted or denied.

If the device fails compliance checks, access may be:

- Denied
- Limited
- Redirected to a remediation network

---

# Authentication

Authentication verifies the identity of the user or device.

Common authentication methods include:

- Username and Password
- Multi-Factor Authentication (MFA)
- Digital Certificates
- 802.1X Authentication

---

# Device Compliance Checks

Before granting access, NAC may verify whether a device:

- Has updated antivirus software
- Has the latest operating system patches
- Has an enabled firewall
- Uses disk encryption
- Meets company security policies

Non-compliant devices may be quarantined until issues are resolved.

---

# Authorization

After successful authentication, NAC determines what resources the device is allowed to access.

Examples:

- HR employees → HR applications only
- Finance employees → Finance servers only
- Guests → Internet access only
- IT administrators → Administrative systems

Authorization follows the **Principle of Least Privilege**.

---

# 802.1X Authentication

802.1X is an IEEE standard used for port-based network access control.

It ensures that devices must authenticate before they can communicate on the network.

Three main components are involved:

- Supplicant (User or Device)
- Authenticator (Switch or Wireless Access Point)
- Authentication Server (Usually a RADIUS Server)

If authentication succeeds, network access is granted.

---

# RADIUS Server

Remote Authentication Dial-In User Service (RADIUS) is a centralized authentication server commonly used with 802.1X.

RADIUS provides:

- Authentication
- Authorization
- Accounting (AAA)

It allows organizations to manage user access from a central location.

---

# Bring Your Own Device (BYOD)

BYOD allows employees to use personal devices for work.

Examples:

- Personal laptops
- Smartphones
- Tablets

While convenient, BYOD introduces security risks because personal devices may not meet organizational security standards.

NAC helps reduce these risks by verifying device compliance before granting access.

---

# Guest Networks

Visitors often require Internet access but should not have access to internal company resources.

A Guest Network is a separate network designed specifically for visitors.

Characteristics include:

- Internet access only
- No access to internal servers
- Isolated from corporate devices
- Limited permissions

---

# Quarantine Network

If a device fails compliance checks, it may be placed in a quarantine network.

The quarantine network allows the device to:

- Download updates
- Install antivirus
- Apply security patches

Once compliant, the device can reconnect to the main network.

---

# Benefits of NAC

Implementing NAC provides:

- Stronger Access Control
- Improved Device Visibility
- Reduced Insider Threats
- Better Compliance
- Protection against Unauthorized Devices
- Reduced Malware Spread

---

# Challenges of NAC

Organizations may face challenges such as:

- Complex deployment
- Higher implementation costs
- Device compatibility issues
- Ongoing policy management

Despite these challenges, NAC significantly improves enterprise security.

---

# Why This Matters to a SOC Analyst

SOC analysts investigate alerts involving unauthorized devices, suspicious logins, and policy violations.

Understanding NAC helps analysts:

- Identify unauthorized network access.
- Investigate authentication failures.
- Detect rogue devices.
- Monitor compliance violations.
- Recommend stronger access control policies.

NAC is an important layer of enterprise security because preventing unauthorized access is often easier than responding to an attack after it occurs.
