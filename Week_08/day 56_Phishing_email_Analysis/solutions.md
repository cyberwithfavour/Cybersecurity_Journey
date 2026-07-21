# Day 56 – Solutions

## Task 1

### Phishing Email Analysis

The process of examining a suspicious email to determine whether it is malicious and identifying the techniques used by the attacker.

---

### Email Header

The technical information attached to an email that contains details about its origin, routing, authentication, and delivery.

---

### Return-Path

The email address where non-delivery reports (bounce messages) are sent. It can help identify the true sender.

---

### Message-ID

A unique identifier assigned to an email message, useful for tracking and investigating email communications.

---

### Indicator of Compromise (IOC)

A piece of evidence that suggests a system or network may have been compromised, such as a malicious domain, IP address, or file hash.

---

### Threat Intelligence

Information collected about known cyber threats that helps analysts identify malicious domains, IP addresses, malware, and attacker behavior.

---

### Safe Attachment

A security feature that scans email attachments for malicious content before allowing users to open them.

---

### Safe Link

A security feature that checks URLs in emails to determine whether they are malicious before users visit them.

---

## Task 2

| Investigation Step | Purpose |
|--------------------|---------|
| Verify Sender | Confirm the sender's identity and detect spoofing. |
| Analyze Subject | Identify urgency or social engineering tactics. |
| Inspect Email Header | Examine routing information and authentication results. |
| Examine URLs | Identify malicious or deceptive links. |
| Analyze Attachments | Detect malware or malicious files. |
| Check SPF/DKIM/DMARC | Verify email authenticity. |
| Search Threat Intelligence | Determine whether domains, IPs, or hashes are known to be malicious. |
| Determine Impact | Assess the risk and decide on the appropriate response. |

---

## Task 3

### 1. Why should a SOC analyst examine the email header instead of relying only on the sender's display name?

Because attackers can easily fake the display name, while the email header contains technical details that help verify the true source of the message.

---

### 2. Why should suspicious links be analyzed before they are opened?

Opening a malicious link may lead to credential theft, malware installation, or phishing websites. Analyzing the link first helps determine whether it is safe.

---

### 3. Can an email still be malicious if SPF, DKIM, and DMARC all pass?

Yes. If an attacker compromises a legitimate email account, the email may successfully pass authentication checks while still being malicious.

---

### 4. Why is threat intelligence important during phishing investigations?

Threat intelligence helps analysts quickly determine whether a domain, IP address, URL, or file hash has previously been associated with malicious activity.

---

## Task 4

### Six Indicators of a Malicious Email

- The sender's domain contains a misspelling (**payr0ll-company.com**).
- The message creates a false sense of urgency.
- It pressures the user to act within **30 minutes**.
- The link points to an unrelated domain (**secure-payroll-login.xyz**).
- It requests account verification unexpectedly.
- The message encourages immediate action without following normal company procedures.

---

### What type of phishing attack is this?

Spear Phishing targeting employees.

---

### What evidence would you collect?

- Complete email header.
- Sender's email address.
- Return-Path.
- Embedded URL.
- SPF, DKIM, and DMARC results.
- Domain reputation.
- URL reputation.
- Any attachments (if present).

---

### Severity Classification

**High**

The email targets employee credentials and could lead to unauthorized access to payroll systems if successful.

---

### Recommended SOC Actions

- Block the malicious sender and domain.
- Block the URL using email and web security tools.
- Search for similar emails across the organization.
- Notify affected users.
- Report the phishing campaign.
- Monitor for compromised accounts.

---

## Task 5

### VirusTotal

**Primary Purpose**

Analyze files, URLs, IP addresses, and domains for malicious activity.

**Information Provided**

- Antivirus detections
- Domain reputation
- URL analysis
- Community comments

**Common SOC Use Case**

Determine whether an attachment or URL is malicious.

---

### AbuseIPDB

**Primary Purpose**

Identify malicious IP addresses.

**Information Provided**

- Abuse reports
- Reputation score
- Geographic information

**Common SOC Use Case**

Investigate suspicious IP addresses found in logs.

---

### URLhaus

**Primary Purpose**

Track malicious URLs used for malware distribution.

**Information Provided**

- Malicious URLs
- Associated malware
- Hosting information

**Common SOC Use Case**

Validate phishing or malware links.

---

### AlienVault OTX

**Primary Purpose**

Threat intelligence sharing platform.

**Information Provided**

- Indicators of Compromise (IOCs)
- Threat reports
- Community intelligence
- Malware indicators

**Common SOC Use Case**

Search for known malicious indicators during investigations.

---

## Practical Exercise

### Safe Investigation Process

Instead of opening the suspicious URL directly:

1. Submit the URL to **VirusTotal** to determine whether security vendors classify it as malicious.
2. Search **URLhaus** to see if the URL has been associated with malware distribution.
3. Check **AbuseIPDB** for the hosting IP address to determine whether it has been reported for malicious activity.

### Why This Matters

These tools allow SOC analysts to investigate potentially malicious URLs without interacting with them directly, reducing the risk of compromising their own systems while gathering valuable intelligence for the investigation.
