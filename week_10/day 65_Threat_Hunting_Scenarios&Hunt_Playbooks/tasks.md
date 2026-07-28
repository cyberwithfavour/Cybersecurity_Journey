# Day 65 – Practical Investigation

## Scenario

You are the Threat Hunter on duty.

Over the past 24 hours, your organization has **not received any high-severity alerts**, but several low-level events have caught your attention.

The events individually seem harmless, but together they may indicate an active attack.

### Observed Activities

- Microsoft Word launched **powershell.exe** on one workstation.
- PowerShell downloaded a file from **hxxp://update-security365[.]com/update.ps1**.
- A new local administrator account named **backup_admin** was created.
- The account logged into two file servers within ten minutes.
- A ZIP archive named **Finance_Backup.zip** was created.
- The archive was uploaded to **mega.nz**.
- Defender did **not** generate a malware alert.

Your manager asks you to perform a complete threat hunt using a structured hunt playbook.

---

# Practical Tasks

## Step 1 – Select the Hunt Playbooks

Determine which hunt playbooks apply to this investigation.

Examples include:

- PowerShell Abuse
- Credential Theft
- Lateral Movement
- Persistence
- Data Exfiltration

Briefly explain why each playbook is relevant.

---

## Step 2 – Build Hunting Hypotheses

Write one hypothesis for each selected playbook.

Example:

> "An attacker may be abusing PowerShell to download and execute malicious scripts."

Repeat this process for the remaining playbooks.

---

## Step 3 – Identify Evidence

For each playbook, identify:

- The evidence already available.
- Additional evidence you still need to collect.
- Which logs or security tools will provide that evidence.

Present your findings in a table.

---

## Step 4 – Build an Investigation Timeline

Arrange all observed activities in chronological order.

Show how the attack progressed from initial execution to possible data exfiltration.

---

## Step 5 – MITRE ATT&CK Mapping

Map every observed behavior to:

- ATT&CK Tactic
- ATT&CK Technique
- ATT&CK ID

Create a complete mapping table.

---

## Step 6 – Determine the Attack Stage

Based on your investigation, determine:

- Has the attacker achieved persistence?
- Has lateral movement occurred?
- Has credential theft likely occurred?
- Has data exfiltration occurred?

Support each answer with evidence.

---

## Step 7 – Detection Engineering

Recommend **eight** new detection rules that would have detected this attack earlier.

Examples:

- Alert when Microsoft Office launches PowerShell.
- Alert when new local administrator accounts are created.
- Alert when ZIP files are uploaded to cloud storage.

Add five more recommendations.

---

## Step 8 – Threat Hunting Report

Prepare a complete Threat Hunting Report containing:

- Executive Summary
- Hunt Playbooks Used
- Hunting Hypotheses
- Evidence Collected
- MITRE ATT&CK Mapping
- Investigation Timeline
- Findings
- Risk Assessment
- Recommended Detection Improvements
- Final Conclusion

---

# GitHub Deliverable

Create the following folder structure:

```text
Week10/
└── Day65_Threat_Hunting_Playbooks/
    ├── hunt_playbooks.md
    ├── hunting_hypotheses.md
    ├── evidence_collection.md
    ├── attack_timeline.md
    ├── mitre_mapping.md
    ├── detection_engineering.md
    └── threat_hunting_report.md
```

---

# Objective

By completing this practical, you should be able to:

- Choose the correct hunt playbooks for an investigation.
- Develop multiple hunting hypotheses.
- Collect and correlate evidence from different data sources.
- Map attacker behaviors to MITRE ATT&CK.
- Assess attack progression and impact.
- Recommend new detection rules.
- Produce a professional Threat Hunting Report suitable for your GitHub portfolio.
