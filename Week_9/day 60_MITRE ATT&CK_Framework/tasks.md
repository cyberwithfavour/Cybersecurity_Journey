# Day 60 – Practical Investigation

## Scenario

You are a Tier 1 SOC Analyst working the morning shift.

At **09:15 AM**, Microsoft Defender generates multiple alerts for an employee's laptop.

The alerts show the following sequence:

- A phishing email was delivered.
- The user opened the attachment.
- Microsoft Word spawned PowerShell.
- PowerShell downloaded a malicious executable.
- LSASS memory was accessed.
- Credentials were dumped.
- The attacker authenticated to another workstation.
- HR documents were compressed into a ZIP file.
- The ZIP file was uploaded to Dropbox.

Your SOC manager wants you to investigate the incident using the MITRE ATT&CK Framework.

---

# Practical Tasks

## Step 1 — Build the Attack Timeline

Create a timeline showing each attacker action in the correct order.

Example:

09:15

↓

09:17

↓

09:20

Continue until the attack is complete.

---

## Step 2 — Map the Attack

Using the MITRE ATT&CK Framework, identify:

- ATT&CK Tactic
- ATT&CK Technique

for every attacker action.

Create your findings in a table.

---

## Step 3 — Identify Detection Opportunities

As the SOC analyst, determine **where the attack could have been detected** before it progressed.

Examples include:

- Email gateway
- Endpoint protection
- PowerShell monitoring
- Credential dumping detection

Find as many detection points as possible.

---

## Step 4 — Containment Plan

Assume the attack is still active.

Write the immediate actions you would take during the first 30 minutes.

Consider:

- User account
- Endpoint
- Network
- Servers
- Evidence preservation

---

## Step 5 — Incident Report

Create a professional SOC Incident Report containing:

- Incident Summary
- Timeline
- MITRE ATT&CK Mapping
- Indicators of Compromise (IoCs)
- Impact Assessment
- Containment Actions
- Lessons Learned

---

# GitHub Deliverable

Create a folder:

```
Week09/
└── Day60_MITRE_Investigation/
```

Inside the folder include:

- attack_timeline.md
- mitre_mapping.md
- incident_report.md

---

# Objective

By completing this investigation, you should be able to think like a SOC analyst by reconstructing an attack, mapping it to MITRE ATT&CK, identifying detection opportunities, and documenting your findings professionally.
