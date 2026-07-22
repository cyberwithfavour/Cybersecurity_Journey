# Day 59 – Solutions

## Task 1

### Network Access Control (NAC)

A security solution that verifies users and devices before allowing them to connect to a network.

---

### Authentication

The process of verifying the identity of a user or device before granting access.

---

### Authorization

The process of determining what resources an authenticated user or device is allowed to access.

---

### Device Compliance

The process of checking whether a device meets an organization's security requirements before network access is granted.

---

### 802.1X Authentication

A port-based network access control standard that requires users or devices to authenticate before communicating on the network.

---

### RADIUS Server

A centralized authentication server that provides Authentication, Authorization, and Accounting (AAA) services.

---

### Guest Network

A separate network designed for visitors that provides Internet access while preventing access to internal company resources.

---

### Quarantine Network

A restricted network where non-compliant devices are placed until security issues are resolved.

---

### Bring Your Own Device (BYOD)

A policy that allows employees to use personal devices for work while enforcing security requirements.

---

## Task 2

| Concept | Purpose |
|---------|---------|
| Network Access Control (NAC) | Controls which users and devices can connect to the network. |
| Authentication | Verifies the identity of users or devices. |
| Authorization | Determines what resources an authenticated user can access. |
| Device Compliance | Ensures devices meet security requirements before connecting. |
| 802.1X | Prevents unauthorized devices from accessing the network. |
| RADIUS Server | Centrally manages authentication, authorization, and accounting. |
| Guest Network | Provides Internet access without exposing internal resources. |
| Quarantine Network | Isolates non-compliant devices until they become secure. |
| BYOD | Allows personal devices while enforcing organizational security policies. |

---

## Task 3

### 1. What is the primary purpose of Network Access Control (NAC)?

To ensure that only authorized users and compliant devices are allowed to access the organization's network.

---

### 2. Why is device compliance important before granting network access?

It reduces the risk of infected, outdated, or insecure devices introducing malware or vulnerabilities into the network.

---

### 3. What is the difference between authentication and authorization?

Authentication verifies **who** the user or device is, while authorization determines **what** that user or device is allowed to access.

---

### 4. Why should guest devices never have access to the internal corporate network?

Because guest devices are not managed by the organization and may introduce malware or provide attackers with access to sensitive resources.

---

### 5. How does 802.1X improve enterprise security?

It prevents unauthorized devices from communicating on the network until they successfully authenticate.

---

## Task 4

### What security control failed?

The organization either did not implement NAC or failed to enforce proper device compliance checks before allowing the personal laptop onto the network.

---

### How could NAC have prevented this incident?

NAC could have verified the laptop's security posture before granting access. If the device failed compliance checks, it would not have been allowed onto the corporate network.

---

### Compliance checks that should have been performed

- Updated antivirus installed
- Latest operating system patches
- Firewall enabled
- Disk encryption enabled
- Device registered with the organization
- No known malware detected

---

### Where should the infected device have been placed?

A **Quarantine Network**, where it could receive updates and malware removal without exposing the internal network.

---

### Recommendations

- Deploy Network Access Control (NAC).
- Require 802.1X authentication.
- Enforce device compliance checks.
- Isolate BYOD devices from critical systems.
- Continuously monitor connected devices.
- Separate guest and personal devices from corporate resources.

---

## Task 5

### Username & Password

**Purpose**

Verifies a user's identity using credentials.

**Advantage**

Simple and widely supported.

**Example**

Logging into a company workstation.

---

### Multi-Factor Authentication (MFA)

**Purpose**

Adds an additional verification step beyond a password.

**Advantage**

Provides stronger protection against stolen credentials.

**Example**

Microsoft Authenticator or OTP codes.

---

### Digital Certificates

**Purpose**

Authenticates users or devices using cryptographic certificates.

**Advantage**

More secure than passwords and difficult to forge.

**Example**

Enterprise Wi-Fi authentication.

---

### 802.1X Authentication

**Purpose**

Authenticates users or devices before allowing network communication.

**Advantage**

Blocks unauthorized devices from accessing the network.

**Example**

Corporate wired and wireless networks.

---

## Practical Exercise

### Full Network Access

- IT Administrators
- Company-managed employee devices

---

### Limited Access

- Contractors
- Temporary staff

---

### Devices That Should Undergo Compliance Checks

- Company laptops
- Personal laptops (BYOD)
- Tablets
- Smartphones

---

### Internet-Only Access

- Guests
- Visitor devices
- Public Wi-Fi users

---

### Devices That Should Be Quarantined

- Missing security patches
- Outdated antivirus
- Firewall disabled
- Malware detected
- Unknown or unauthorized devices

---

### How This NAC Policy Reduces Risk

- Prevents unauthorized users from accessing the network.
- Stops non-compliant devices before they become a threat.
- Protects sensitive business resources.
- Limits malware infections.
- Improves visibility and control over connected devices.
- Strengthens the organization's overall security posture.
