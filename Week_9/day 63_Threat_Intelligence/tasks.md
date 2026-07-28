# Day 63 – Practical Investigation

## Scenario

You are a Tier 1 SOC Analyst working the morning shift.

Your Threat Intelligence Platform (TIP) receives the following intelligence from multiple trusted sources:

### Intelligence Feed

**Threat Actor:** APT-Shadow

**Campaign:** Operation Silent Invoice

**Known IoCs**

**Malicious IPs**

- 185.220.101.45
- 91.214.124.77

**Domains**

- secure-update365.com
- microsoft-login365.net

**SHA256 Hash**

```
8f7dbe5d8d6c9e5e0a43cdd93e4c2fd10d8bb9c3f2adbaec2f8d1c6a7c18f421
```

**Known TTPs**

- Spear Phishing
- PowerShell Execution
- Credential Dumping
- Remote Services
- Data Exfiltration via Cloud Storage

---

Meanwhile, your SIEM reports the following activities inside your organization:

- One workstation communicated with **185.220.101.45**
- Two users visited **secure-update365.com**
- A file with the provided SHA256 hash was detected on one endpoint
- Microsoft Word launched PowerShell
- Dropbox uploads were detected from the Finance department

Your manager asks you to determine whether your organization is part of the ongoing campaign.

---

# Practical Tasks

## Step 1 – Threat Intelligence Validation

Compare the SIEM findings with the Threat Intelligence feed.

Determine:

- Which alerts match the intelligence feed.
- Which alerts require further investigation.
- Which systems appear compromised.

---

## Step 2 – Threat Actor Profile

Create a profile for **APT-Shadow** containing:

- Threat Actor Name
- Campaign Name
- Known Targets
- Common TTPs
- Risk Level
- Possible Objectives

---

## Step 3 – Build an IOC Watchlist

Create an IOC watchlist that your SOC can immediately deploy.

Include:

- IP Addresses
- Domains
- File Hashes
- Suspicious Behaviors

---

## Step 4 – Threat Hunt

Assume the campaign has been active for one week.

Document how you would hunt for additional compromised systems.

Consider searching for:

- Connections to malicious IPs
- DNS requests
- PowerShell execution
- File hashes
- Cloud storage uploads
- Credential dumping activity

---

## Step 5 – Immediate Response

As the responding SOC analyst, document the actions you would take within the first hour.

Include:

- Blocking actions
- Endpoint actions
- User account actions
- Network actions
- Escalation

---

## Step 6 – Intelligence Report

Prepare a Threat Intelligence Report containing:

- Executive Summary
- Threat Actor Overview
- Campaign Description
- Indicators of Compromise
- MITRE ATT&CK Techniques Observed
- Systems Affected
- Risk Assessment
- Recommended Defensive Actions

---

# GitHub Deliverable

Create the following folder structure:

```text
Week09/
└── Day63_Threat_Intelligence/
    ├── threat_actor_profile.md
    ├── ioc_watchlist.md
    ├── threat_hunt.md
    ├── response_plan.md
    └── threat_intelligence_report.md
```

---

# Objective

By completing this investigation, you should be able to:

- Validate Threat Intelligence against SIEM alerts.
- Correlate IoCs with real-world events.
- Build an IOC watchlist.
- Conduct a basic threat hunt.
- Produce a professional Threat Intelligence Report suitable for your SOC portfolio.
