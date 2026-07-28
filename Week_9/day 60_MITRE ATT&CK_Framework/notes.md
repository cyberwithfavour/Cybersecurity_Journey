# Day 60 – MITRE ATT&CK Framework

## Objective

Understand how security teams use the MITRE ATT&CK Framework to analyze, investigate, detect, and respond to real-world cyberattacks.

---

# What is MITRE?

**MITRE** is a non-profit organization that conducts cybersecurity research and develops frameworks, tools, and best practices used by governments and private organizations worldwide.

One of its most influential contributions is the **MITRE ATT&CK Framework**.

---

# What is MITRE ATT&CK?

**MITRE ATT&CK** stands for:

> **Adversarial Tactics, Techniques & Common Knowledge**

It is a globally recognized knowledge base that documents how real attackers behave during cyberattacks.

Instead of focusing on malware itself, ATT&CK focuses on **attacker behavior**.

---

# Why Was MITRE ATT&CK Created?

Before ATT&CK, security teams often described attacks differently.

MITRE created ATT&CK to provide:

- A common language for defenders
- Standardized attack mapping
- Better threat intelligence
- Improved detection engineering
- More effective incident response

---

# ATT&CK Matrix

The ATT&CK Matrix organizes attacker behavior into different stages called **Tactics**.

Each tactic contains several **Techniques**, and some techniques are further divided into **Sub-techniques**.

Think of the matrix as a roadmap showing every step an attacker may take during an attack.

---

# ATT&CK Tactics

The Enterprise ATT&CK Matrix currently contains the following tactics:

1. Initial Access
2. Execution
3. Persistence
4. Privilege Escalation
5. Defense Evasion
6. Credential Access
7. Discovery
8. Lateral Movement
9. Collection
10. Command and Control
11. Exfiltration
12. Impact

Each tactic answers one question:

> **"What is the attacker's objective at this stage?"**

---

# Techniques

Techniques describe **how** an attacker accomplishes a tactic.

Example:

### Tactic

Initial Access

### Technique

Phishing

Another example:

### Tactic

Credential Access

### Technique

OS Credential Dumping

---

# Sub-techniques

Some techniques are very broad.

MITRE breaks them into smaller actions called **Sub-techniques**.

Example:

Technique:

- PowerShell

Sub-technique:

- PowerShell Script Execution

Another example:

Technique:

- Phishing

Sub-techniques:

- Spearphishing Attachment
- Spearphishing Link
- Spearphishing via Service

---

# Procedures

A **Procedure** is the actual method used by an attacker.

Example:

Technique:

PowerShell

Procedure:

```
powershell.exe -EncodedCommand ...
```

Different attackers may use the same technique but different procedures.

---

# TTPs

A very common cybersecurity term is:

**TTPs**

It stands for:

- Tactics
- Techniques
- Procedures

SOC analysts frequently describe attacker behavior using TTPs.

---

# ATT&CK IDs

Every technique in MITRE ATT&CK has a unique identifier.

Examples:

| Technique | ATT&CK ID |
|-----------|-----------|
| Phishing | T1566 |
| PowerShell | T1059.001 |
| Credential Dumping | T1003 |
| Remote Services | T1021 |

These IDs create a universal language for security professionals.

---

# Example Mapping

Imagine the following attack:

Employee opens a phishing email.

↓

Word launches PowerShell.

↓

PowerShell downloads malware.

↓

Credentials are dumped.

↓

Attacker connects to another workstation.

↓

Sensitive files are compressed.

↓

Files are uploaded to Dropbox.

Every one of these actions can be mapped directly to a MITRE ATT&CK technique.

---

# Why SOC Analysts Use MITRE ATT&CK

SOC analysts use ATT&CK to:

- Investigate security incidents
- Perform threat hunting
- Write detection rules
- Build SIEM alerts
- Improve defensive strategies
- Understand attacker behavior
- Communicate findings using a common language

---

# MITRE ATT&CK vs Malware Analysis

## Malware Analysis

Focuses on:

- The malware itself
- Code behavior
- Reverse engineering

## MITRE ATT&CK

Focuses on:

- Attacker behavior
- Attack techniques
- Detection opportunities
- Defensive strategies

---

# MITRE ATT&CK Navigator

MITRE provides a free tool called **ATT&CK Navigator**.

Security teams use it to:

- Highlight observed techniques
- Map attacks
- Compare threat actors
- Visualize detections
- Plan defensive improvements

---

# Real-World Example

A SOC analyst receives the following alerts:

- Phishing email detected
- PowerShell executed
- Credential dumping observed
- Remote login detected
- Dropbox upload detected

Instead of viewing these as separate alerts, MITRE ATT&CK helps the analyst connect them into one complete attack story.

---

# Why This Matters

Modern SOCs don't simply investigate malware.

They investigate **attacker behavior**.

MITRE ATT&CK helps analysts answer questions such as:

- How did the attacker get in?
- What techniques were used?
- Where could we have detected them?
- How can we stop similar attacks in the future?

---

# Key Takeaways

- MITRE ATT&CK is a framework for understanding attacker behavior.
- It provides a common language for defenders worldwide.
- ATT&CK organizes attacks into **Tactics**, **Techniques**, and **Sub-techniques**.
- Every technique has a unique ATT&CK ID.
- SOC analysts use ATT&CK during investigations, threat hunting, and detection engineering.
- Understanding MITRE ATT&CK is an essential skill for every SOC analyst.
