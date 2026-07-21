# Day 56 – Notes

## Phishing Email Analysis

Phishing email analysis is the process of examining suspicious emails to determine whether they are malicious and identifying the techniques used by attackers.

SOC analysts investigate phishing emails to protect users, prevent credential theft, stop malware infections, and gather indicators of compromise (IOCs).

---

## Why Phishing Analysis Matters

A single successful phishing email can lead to:

- Credential theft
- Malware infection
- Ransomware deployment
- Business Email Compromise (BEC)
- Data exfiltration
- Financial fraud

Early detection helps reduce the impact of an attack.

---

## The SOC Phishing Investigation Process

A typical phishing investigation follows these steps:

1. Receive the reported email.
2. Preserve the original message.
3. Analyze the email header.
4. Examine the sender.
5. Inspect URLs.
6. Analyze attachments.
7. Check authentication results.
8. Search threat intelligence.
9. Determine impact.
10. Recommend response actions.

---

## Step 1 — Verify the Sender

Do not trust the display name.

Example:

Display Name:

```
Microsoft Support
```

Actual Email:

```
microsoft-support@gmail.com
```

Always verify the actual email address.

---

## Step 2 — Analyze the Subject Line

Attackers often create urgency.

Examples:

- Password Expiring
- Urgent Invoice
- Immediate Payment Required
- Verify Your Account
- Payroll Update

Urgency encourages users to act without thinking.

---

## Step 3 — Inspect the Email Header

The email header provides technical information including:

- From
- Return-Path
- Received
- Message-ID
- SPF Result
- DKIM Result
- DMARC Result

Headers often reveal spoofing attempts.

---

## Step 4 — Examine URLs

Never trust the visible link.

Example:

Displayed:

```
https://microsoft.com
```

Actual destination:

```
http://secure-login.verify-account.ru
```

Always inspect where the link actually points.

---

## Step 5 — Analyze Attachments

Common malicious attachment types include:

- .zip
- .iso
- .html
- .docm
- .xlsm
- .exe
- .js

Office files containing macros should always be treated with caution.

---

## Step 6 — Verify SPF, DKIM and DMARC

These authentication checks help determine whether the sender is legitimate.

Example:

```
SPF: PASS

DKIM: PASS

DMARC: PASS
```

Passing authentication does not guarantee an email is safe, but failing these checks increases suspicion.

---

## Step 7 — Search Threat Intelligence

Investigate:

- Sender domain
- URLs
- IP addresses
- Attachment hashes

Useful threat intelligence sources include:

- VirusTotal
- URLhaus
- AbuseIPDB
- AlienVault OTX

---

## Indicators of a Malicious Email

SOC analysts commonly look for:

- Unknown sender
- Misspelled domains
- Urgent language
- Credential requests
- Unexpected attachments
- Suspicious links
- Poor grammar
- Unexpected payment requests
- Authentication failures

---

## Email Investigation Outcome

After completing the investigation, analysts determine whether the email is:

- Legitimate
- Spam
- Phishing
- Spear Phishing
- Business Email Compromise
- Malware Delivery

The analyst then recommends appropriate containment and response actions.

---

## Why This Matters to a SOC Analyst

Email investigations are among the most common alerts handled in a SOC.

Being able to quickly identify phishing attempts, analyze email headers, validate authentication results, and determine the severity of an email-based threat is a core skill for every SOC analyst.
