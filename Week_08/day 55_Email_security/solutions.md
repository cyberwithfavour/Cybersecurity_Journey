# Day 55 – Solutions

## Task 1

### Spam

Unsolicited bulk email, usually sent for advertising or other unwanted purposes. Some spam messages may contain malicious links or attachments.

---

### Phishing

A social engineering attack that attempts to trick users into revealing sensitive information such as usernames, passwords, or financial details.

---

### Spear Phishing

A targeted phishing attack directed at a specific person or organization using personalized information.

---

### Whaling

A phishing attack specifically targeting senior executives or other high-profile individuals within an organization.

---

### Business Email Compromise (BEC)

An attack where criminals impersonate trusted individuals or organizations to trick victims into sending money or confidential information.

---

### Email Spoofing

The act of forging an email sender's address to make the message appear to come from a trusted source.

---

### SPF

Sender Policy Framework (SPF) is an email authentication protocol that specifies which mail servers are authorized to send emails for a domain.

---

### DKIM

DomainKeys Identified Mail (DKIM) uses digital signatures to verify that an email has not been altered during transmission.

---

### DMARC

Domain-based Message Authentication, Reporting & Conformance (DMARC) tells receiving mail servers how to handle emails that fail SPF or DKIM checks and provides reporting.

---

## Task 2

| Attack | Target | Goal | Example |
|---------|---------|------|---------|
| Spam | General users | Advertising or malware distribution | Promotional emails |
| Phishing | General users | Steal credentials | Fake Microsoft login email |
| Spear Phishing | Specific individual | Gain unauthorized access | Personalized HR email |
| Whaling | Executives | Financial fraud or sensitive information | Fake board meeting request |
| Business Email Compromise (BEC) | Finance or executives | Fraudulent money transfer | Fake CEO payment request |

---

## Task 3

### 1. Why is phishing considered one of the biggest cybersecurity threats?

Because it exploits human trust rather than technical vulnerabilities, making it effective even against organizations with strong security controls.

---

### 2. What is the primary difference between phishing and spear phishing?

Phishing targets many users with generic messages, while spear phishing targets a specific individual using personalized information.

---

### 3. Why do organizations implement SPF, DKIM, and DMARC together instead of using only one of them?

Because they complement each other. SPF verifies sending servers, DKIM verifies message integrity, and DMARC enforces policies and reporting. Together they provide stronger protection against email spoofing.

---

### 4. How can Multi-Factor Authentication (MFA) reduce the impact of phishing attacks?

Even if an attacker steals a user's password through phishing, MFA requires an additional verification factor before access is granted, making unauthorized access much more difficult.

---

## Task 4

### Five Indicators of Suspicious Activity

- The sender uses a Gmail address instead of the company's official domain.
- The message creates urgency.
- The request involves transferring money.
- The request asks to bypass normal approval procedures.
- The email provides no verification method and asks for immediate action.

---

### What type of attack is this?

Business Email Compromise (BEC).

---

### What would you investigate first?

- Verify the sender's email address.
- Check the email header.
- Review SPF, DKIM, and DMARC results.
- Contact the CEO through another trusted communication channel.
- Determine whether similar emails were sent to other employees.

---

### What actions should you take?

- Prevent the payment from being processed.
- Report the email as phishing.
- Block the sender if malicious.
- Notify affected departments.
- Escalate the incident according to the incident response process.

---

## Task 5

### Microsoft Defender for Office 365

**Primary Purpose**

Protects Microsoft 365 email from phishing, malware, and malicious links.

**Key Feature**

Safe Links and Safe Attachments.

**Vendor**

Microsoft.

---

### Proofpoint

**Primary Purpose**

Enterprise email security.

**Key Feature**

Advanced phishing detection.

**Vendor**

Proofpoint.

---

### Mimecast

**Primary Purpose**

Cloud email security and continuity.

**Key Feature**

Email threat protection and archiving.

**Vendor**

Mimecast.

---

### Cisco Secure Email

**Primary Purpose**

Secure enterprise email communications.

**Key Feature**

Spam, malware, and phishing protection.

**Vendor**

Cisco.

---

## Practical Exercise

### Common Email Header Fields

- **From** – Displays the sender's email address.
- **To** – Displays the recipient's email address.
- **Subject** – Displays the email subject.
- **Return-Path** – Shows where bounce messages are sent.
- **Received** – Records the path the email took through mail servers.
- **SPF Result** – Indicates whether the sender passed SPF validation.
- **DKIM Result** – Indicates whether the email signature is valid.
- **DMARC Result** – Indicates whether the email complies with the sender's DMARC policy.

### Why are email headers valuable?

Email headers help SOC analysts verify the true sender, trace the email's route, detect spoofing attempts, validate authentication results, and gather evidence during phishing investigations.
