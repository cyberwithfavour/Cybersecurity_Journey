# Day 63 – Threat Intelligence (Deep Dive)

## Objective

Understand the fundamentals of Cyber Threat Intelligence (CTI), its different types, intelligence lifecycle, intelligence sources, and how SOC analysts use threat intelligence to detect, investigate, and respond to cyber threats.

---

# What is Threat Intelligence?

Threat Intelligence (TI) is evidence-based knowledge about existing or emerging cyber threats.

It provides context about:

- Threat Actors
- Indicators of Compromise (IoCs)
- Tactics, Techniques and Procedures (TTPs)
- Vulnerabilities
- Malware
- Campaigns

Threat Intelligence helps organizations make informed security decisions instead of reacting blindly to attacks.

---

# Why is Threat Intelligence Important?

Without Threat Intelligence, security teams only respond after attacks occur.

Threat Intelligence helps organizations:

- Identify emerging threats
- Detect attacks earlier
- Improve investigations
- Strengthen defenses
- Prioritize risks
- Hunt for threats proactively

---

# Types of Threat Intelligence

## 1. Strategic Intelligence

Designed for executives and management.

Focuses on:

- Business risks
- Industry trends
- Nation-state threats
- Long-term planning

Example:

"Ransomware attacks against healthcare organizations increased by 45% this year."

---

## 2. Operational Intelligence

Focuses on ongoing attacks.

Answers questions like:

- Who is attacking?
- Why are they attacking?
- What are their objectives?

Example:

A threat actor targeting financial institutions with phishing campaigns.

---

## 3. Tactical Intelligence

Focuses on attacker behavior.

Includes:

- MITRE ATT&CK mappings
- TTPs
- Malware behavior
- Attack techniques

Used heavily by SOC analysts.

---

## 4. Technical Intelligence

Contains technical artifacts such as:

- IP addresses
- Domains
- URLs
- File hashes
- Email addresses
- SSL certificates

Usually has a short lifespan because attackers frequently change these indicators.

---

# Threat Intelligence Lifecycle

Threat Intelligence follows a structured lifecycle.

## 1. Planning

Define intelligence requirements.

Questions include:

- What threats concern us?
- Which assets require protection?

---

## 2. Collection

Gather intelligence from multiple sources.

Examples:

- Threat feeds
- Security vendors
- OSINT
- Government advisories
- Internal logs

---

## 3. Processing

Organize collected information into usable formats.

Examples:

- Remove duplicates
- Validate indicators
- Normalize data

---

## 4. Analysis

Transform raw data into actionable intelligence.

Example:

Determine whether a malicious IP belongs to a ransomware campaign.

---

## 5. Dissemination

Share intelligence with the appropriate audience.

Examples:

- SOC Team
- Incident Response Team
- Management

---

## 6. Feedback

Evaluate whether the intelligence met organizational needs.

Improve future intelligence collection.

---

# Threat Intelligence Sources

Common sources include:

## Open Source Intelligence (OSINT)

Publicly available information.

Examples:

- Security blogs
- GitHub
- News articles
- Research papers

---

## Commercial Threat Intelligence

Paid intelligence feeds.

Examples:

- Recorded Future
- CrowdStrike Intelligence
- Microsoft Threat Intelligence

---

## Government Intelligence

Examples:

- CISA
- NCSC
- CERT
- FBI Flash Alerts

---

## Internal Intelligence

Generated from:

- SIEM logs
- Firewall logs
- EDR alerts
- Incident investigations

---

# Threat Intelligence Platforms (TIPs)

A Threat Intelligence Platform helps organizations collect, manage, enrich, and distribute threat intelligence.

Examples include:

- MISP
- OpenCTI
- ThreatConnect
- Anomali

---

# Threat Intelligence in a SOC

SOC analysts use Threat Intelligence to:

- Investigate alerts
- Validate IoCs
- Identify threat actors
- Prioritize incidents
- Hunt threats
- Improve detections

---

# Threat Intelligence vs Threat Hunting

## Threat Intelligence

Provides information about known threats.

Example:

"This IP address belongs to a ransomware operator."

---

## Threat Hunting

Searches for unknown threats inside the environment.

Example:

"Has any endpoint communicated with this malicious IP?"

Threat Intelligence supports Threat Hunting.

---

# Threat Intelligence vs Vulnerability Intelligence

Threat Intelligence focuses on:

- Attackers
- Campaigns
- Malware
- IoCs
- TTPs

Vulnerability Intelligence focuses on:

- CVEs
- Software weaknesses
- Exploitation likelihood
- Patch priorities

---

# Intelligence Sharing Standards

Organizations share Threat Intelligence using standardized formats.

Common standards include:

- STIX (Structured Threat Information Expression)
- TAXII (Trusted Automated eXchange of Indicator Information)

These standards allow different security tools to exchange intelligence automatically.

---

# Intelligence Decay

Threat Intelligence loses value over time.

Example:

A malicious IP address may only be active for a few days before attackers abandon it.

Behavioral intelligence (TTPs) generally remains useful much longer than technical indicators.

---

# Real-World Example

Microsoft Defender detects communication with:

```
185.220.101.45
```

Threat Intelligence reveals:

- Associated with ransomware
- Used in previous attacks
- Linked to a known threat actor
- Active Command & Control server

The SOC immediately:

- Blocks the IP
- Hunts for additional infected devices
- Reviews historical logs
- Escalates the incident

---

# Why This Matters

Threat Intelligence transforms raw security alerts into meaningful information.

Instead of simply seeing:

> "Connection detected."

A SOC analyst can determine:

- Who the attacker is.
- What campaign they belong to.
- Which techniques they are using.
- How dangerous the threat is.
- What actions should be taken next.

---

# Key Takeaways

- Threat Intelligence is evidence-based information about cyber threats.
- There are four primary types: Strategic, Operational, Tactical, and Technical.
- The Threat Intelligence Lifecycle consists of Planning, Collection, Processing, Analysis, Dissemination, and Feedback.
- Threat Intelligence helps SOC teams investigate, detect, prioritize, and respond to cyber threats.
- Technical indicators change quickly, but attacker behaviors (TTPs) remain valuable for much longer.
- Threat Intelligence becomes most effective when combined with SIEM, EDR, MITRE ATT&CK, and Threat Hunting.
