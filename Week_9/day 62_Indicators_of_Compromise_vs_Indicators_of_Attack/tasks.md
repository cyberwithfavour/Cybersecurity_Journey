# Day 62 – Practical Investigation

## Scenario

You are the Tier 1 SOC Analyst on the morning shift.

Microsoft Defender for Endpoint has generated multiple alerts from an employee's laptop.

The following activities were observed:

- PowerShell executed with an encoded command.
- A connection was established to **185.220.101.45**.
- A file named **invoice_update.exe** was downloaded.
- The file hash is:

```
SHA256:
8f7dbe5d8d6c9e5e0a43cdd93e4c2fd10d8bb9c3f2adbaec2f8d1c6a7c18f421
```

- `lsass.exe` was accessed.
- The user account **finance_admin** logged in to three different workstations within five minutes.
- A ZIP file named **Payroll2026.zip** was created.
- The ZIP file was uploaded to **dropbox.com**.

Your SOC manager has asked you to investigate the incident.

---

# Practical Tasks

## Step 1 – Separate IoCs and IoAs

Create two tables:

### Table 1

Indicators of Compromise (IoCs)

### Table 2

Indicators of Attack (IoAs)

Explain why each item belongs in its respective category.

---

## Step 2 – Threat Prioritization

Rank each finding from **Highest** to **Lowest** priority.

Explain your reasoning.

Example:

| Finding | Priority |
|----------|----------|
| LSASS Access | Critical |

Continue for every alert.

---

## Step 3 – Build an Investigation Timeline

Arrange every event in chronological order.

Your timeline should clearly show how the attack progressed.

---

## Step 4 – Containment

The attacker is still active.

Document the immediate actions you would take during the first 30 minutes.

Include:

- Endpoint actions
- User account actions
- Network actions
- Evidence preservation
- Escalation

---

## Step 5 – Threat Intelligence

Assume you have access to Threat Intelligence feeds.

Identify which IoCs should immediately be searched across the organization.

Examples:

- IP address
- Domain
- File hash
- File name

Explain why each one is valuable.

---

## Step 6 – Detection Improvements

Recommend at least **six new detections** the SOC should implement to identify similar attacks earlier.

Examples:

- Alert when Microsoft Office launches PowerShell.
- Alert on LSASS memory access.

Continue with four more.

---

## Step 7 – SOC Incident Report

Prepare a professional incident report containing:

- Incident Summary
- Timeline
- IoCs Identified
- IoAs Identified
- Risk Assessment
- Containment Actions
- Recommended Improvements

---

# GitHub Deliverable

Create the following folder structure:

```text
Week09/
└── Day62_IOCs_vs_IOAs/
    ├── ioc_analysis.md
    ├── ioa_analysis.md
    ├── investigation_timeline.md
    ├── containment_plan.md
    ├── threat_intelligence.md
    └── incident_report.md
```

---

# Objective

By completing this investigation, you should be able to:

- Differentiate between IoCs and IoAs.
- Prioritize security alerts.
- Build a complete attack timeline.
- Apply threat intelligence during an investigation.
- Recommend stronger detection strategies.
- Produce a SOC-quality incident report suitable for your GitHub portfolio.
