# Day 64 – Practical Investigation

## Scenario

You are a Threat Hunter working in the SOC.

Your organization has **not received any security alerts** today.

However, a new Threat Intelligence report states that a ransomware group is actively targeting financial organizations by abusing **PowerShell** to gain initial access, dump credentials, and move laterally before encrypting files.

Your SOC Manager wants you to perform a **proactive threat hunt** to determine whether the attackers are already inside your environment.

No alerts have been triggered.

Your job is to hunt.

---

# Practical Tasks

## Step 1 – Develop a Hunting Hypothesis

Create a hunting hypothesis based on the Threat Intelligence report.

Your hypothesis should answer:

- What attacker behavior are you looking for?
- Why do you believe it may exist?
- Which systems are most likely to be affected?

---

## Step 2 – Identify Data Sources

List every log source you would use during the hunt.

Examples include:

- Microsoft Sentinel
- Microsoft Defender for Endpoint
- Sysmon
- Windows Event Logs
- DNS Logs
- Firewall Logs
- Active Directory Logs
- Proxy Logs

For each source, explain what evidence you expect to find.

---

## Step 3 – Hunt for Suspicious Behaviors

Search for the following behaviors:

- Microsoft Office spawning PowerShell
- Encoded PowerShell commands
- PowerShell downloading files from the internet
- LSASS access
- New administrator accounts
- Remote Desktop logins outside business hours
- Large outbound data transfers
- Multiple failed logins followed by a successful login

Document every suspicious activity discovered.

---

## Step 4 – Map Findings to MITRE ATT&CK

For every suspicious behavior identified, map it to:

- ATT&CK Tactic
- ATT&CK Technique
- ATT&CK ID

Present your findings in a table.

---

## Step 5 – Determine Whether the Hunt Found a Threat

Based on your investigation, determine whether:

- No threat was identified.
- Suspicious activity requires further investigation.
- Active compromise has been confirmed.

Justify your conclusion using evidence from your hunt.

---

## Step 6 – Detection Improvement

Assume your hunt uncovered new attacker behaviors.

Recommend **at least six** new detection rules the SOC should implement.

Examples:

- Alert when Microsoft Office launches PowerShell.
- Alert on Base64-encoded PowerShell commands.
- Alert when LSASS is accessed by non-system processes.

Continue with three additional detections.

---

## Step 7 – Threat Hunting Report

Prepare a professional Threat Hunting Report containing:

- Hunt Objective
- Hunting Hypothesis
- Data Sources Used
- MITRE ATT&CK Mapping
- Findings
- Evidence Collected
- Risk Assessment
- Recommended Detection Improvements
- Final Conclusion

---

# GitHub Deliverable

Create the following folder structure:

```text
Week09/
└── Day64_Threat_Hunting/
    ├── hunting_hypothesis.md
    ├── data_sources.md
    ├── hunt_findings.md
    ├── mitre_mapping.md
    ├── detection_improvements.md
    └── threat_hunting_report.md
```

---

# Objective

By completing this practical, you should be able to:

- Develop a threat hunting hypothesis.
- Identify the right data sources for a hunt.
- Search for attacker behaviors instead of waiting for alerts.
- Map findings to MITRE ATT&CK.
- Recommend new detections based on your findings.
- Produce a professional Threat Hunting Report suitable for your SOC portfolio.
