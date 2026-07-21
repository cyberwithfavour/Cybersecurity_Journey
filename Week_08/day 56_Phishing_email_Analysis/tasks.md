# Day 56 – Tasks

## Task 1

Define the following terms in your own words.

- Phishing Email Analysis
- Email Header
- Return-Path
- Message-ID
- Indicator of Compromise (IOC)
- Threat Intelligence
- Safe Attachment
- Safe Link

---

## Task 2

Complete the table below.

| Investigation Step | Purpose |
|--------------------|---------|
| Verify Sender | |
| Analyze Subject | |
| Inspect Email Header | |
| Examine URLs | |
| Analyze Attachments | |
| Check SPF/DKIM/DMARC | |
| Search Threat Intelligence | |
| Determine Impact | |

---

## Task 3

Answer the following questions.

### 1.

Why should a SOC analyst examine the email header instead of relying only on the sender's display name?

---

### 2.

Why should suspicious links be analyzed before they are opened?

---

### 3.

Can an email still be malicious if SPF, DKIM, and DMARC all pass? Explain your answer.

---

### 4.

Why is threat intelligence important during phishing investigations?

---

## Task 4

### Think Like a SOC Analyst

A user reports the following email:

**From:**

```
Payroll Department <payroll-update@payr0ll-company.com>
```

**Subject:**

```
Salary Adjustment Notice
```

**Message:**

> Due to recent payroll changes, please verify your employee account within the next 30 minutes to avoid payment delays.

A button in the email says:

```
Verify Account
```

The link points to:

```
http://secure-payroll-login.xyz
```

Answer the following:

- Identify at least **six indicators** that suggest this email is malicious.
- What type of phishing attack is this?
- What evidence would you collect?
- Would you classify this as Low, Medium, High, or Critical severity? Explain your answer.
- What actions should the SOC team take?

---

## Task 5

Research the following threat intelligence platforms.

For each platform, identify:

- Primary Purpose
- Information Provided
- Common SOC Use Case

Platforms:

- VirusTotal
- AbuseIPDB
- URLhaus
- AlienVault OTX

---

## Practical Exercise

Choose any suspicious-looking URL (or use a sample URL from a cybersecurity article).

Without visiting the website, explain how you would investigate it safely using tools such as:

- VirusTotal
- URLhaus
- AbuseIPDB

Describe what information each tool could provide and how it would help determine whether the URL is malicious.
