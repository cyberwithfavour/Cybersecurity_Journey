# Day 55 – Notes

## What is Email Security?

**Email Security** refers to the technologies, policies, and best practices used to protect email systems and users from unauthorized access, phishing, malware, spam, and other email-based attacks.

Since email is one of the most widely used communication methods in organizations, it is also one of the most common attack vectors for cybercriminals.

---

## Why is Email Security Important?

Email security helps organizations:

- Prevent phishing attacks.
- Block malicious attachments.
- Protect sensitive information.
- Detect spoofed emails.
- Prevent malware infections.
- Reduce the risk of Business Email Compromise (BEC).

---

## Common Email Threats

### Spam

Spam refers to unsolicited or unwanted emails, often sent in bulk.

Although many spam emails are harmless advertisements, some contain malicious links or attachments.

---

### Phishing

Phishing is a social engineering attack where an attacker attempts to trick users into revealing sensitive information such as usernames, passwords, or financial details.

Example:

An email claiming to be from Microsoft asks you to "verify your account" through a fake login page.

---

### Spear Phishing

Spear phishing is a targeted phishing attack aimed at a specific individual or organization.

Unlike regular phishing, spear phishing messages are personalized, making them more convincing.

---

### Whaling

Whaling targets high-profile individuals such as:

- CEOs
- Executives
- Directors
- Financial Managers

The goal is usually financial fraud or theft of sensitive information.

---

### Business Email Compromise (BEC)

BEC is an attack where cybercriminals impersonate a trusted employee, executive, or business partner to trick victims into:

- Sending money.
- Changing payment information.
- Sharing confidential data.

BEC attacks often do **not** contain malware or malicious attachments, making them difficult to detect.

---

## Email Authentication

Email authentication helps verify that an email actually came from the claimed sender.

Three important technologies are used:

---

### SPF (Sender Policy Framework)

SPF allows domain owners to specify which mail servers are authorized to send emails on behalf of their domain.

Purpose:

- Prevent email spoofing.

---

### DKIM (DomainKeys Identified Mail)

DKIM digitally signs outgoing emails using cryptographic keys.

Purpose:

- Verify that the email has not been modified during transmission.
- Confirm the sender's identity.

---

### DMARC (Domain-based Message Authentication, Reporting & Conformance)

DMARC works with SPF and DKIM to tell receiving mail servers how to handle emails that fail authentication.

Possible actions:

- None
- Quarantine
- Reject

DMARC also provides reporting so organizations can monitor spoofing attempts.

---

## Indicators of a Suspicious Email

SOC analysts look for:

- Misspelled domain names.
- Unexpected attachments.
- Suspicious links.
- Urgent requests.
- Generic greetings.
- Requests for credentials.
- Requests for payment.
- Poor grammar or spelling.
- Unexpected sender addresses.

---

## Email Security Best Practices

- Enable Multi-Factor Authentication (MFA).
- Implement SPF, DKIM, and DMARC.
- Use secure email gateways.
- Train users to recognize phishing emails.
- Scan attachments for malware.
- Verify payment requests through another communication channel.
- Keep email systems updated.

---

## Email Security in a SOC Environment

SOC analysts investigate:

- Phishing emails.
- Suspicious attachments.
- Malicious URLs.
- Email spoofing.
- Business Email Compromise (BEC).
- Malware delivered through email.
- Unusual outbound email activity.

Email investigations often involve analyzing:

- Email headers.
- Sender IP addresses.
- Authentication results (SPF, DKIM, DMARC).
- Attachment hashes.
- Embedded URLs.
- Threat intelligence feeds.
