# Day 65 – Threat Hunting Scenarios & Hunt Playbooks

## Objective

Learn how SOC analysts perform real-world threat hunts using structured hunt playbooks. Understand common threat hunting scenarios, how to investigate suspicious behaviors, and how to document hunting results.

---

# What is a Threat Hunting Playbook?

A Threat Hunting Playbook is a documented, repeatable guide that helps analysts perform a specific threat hunt.

Instead of starting from scratch every time, analysts follow a structured process.

A playbook typically includes:

- Hunt objective
- Hunting hypothesis
- Data sources
- Investigation steps
- MITRE ATT&CK mapping
- Expected findings
- Detection improvements

---

# Why Use Hunt Playbooks?

Hunt playbooks help SOC teams:

- Standardize investigations
- Improve consistency
- Reduce investigation time
- Train junior analysts
- Document successful hunts
- Improve detection engineering

---

# Common Threat Hunting Scenarios

Modern SOC teams frequently hunt for:

- PowerShell abuse
- Credential dumping
- Phishing compromise
- Lateral movement
- Privilege escalation
- Persistence mechanisms
- Suspicious RDP activity
- Data exfiltration
- Insider threats
- Living-off-the-Land (LotL) attacks

---

# Scenario 1 – PowerShell Abuse

### Hypothesis

An attacker may be abusing PowerShell to execute malicious commands.

### Data Sources

- Sysmon
- PowerShell Logs
- Microsoft Defender
- Microsoft Sentinel

### Hunt For

- Encoded PowerShell commands
- DownloadString()
- Invoke-Expression (IEX)
- Execution Policy Bypass
- Office applications spawning PowerShell

MITRE ATT&CK

- T1059.001 – PowerShell

---

# Scenario 2 – Credential Dumping

### Hypothesis

An attacker may have attempted to steal credentials.

### Hunt For

- LSASS access
- Mimikatz execution
- Suspicious handle requests
- Defender Credential Theft alerts

MITRE ATT&CK

- T1003 – OS Credential Dumping

---

# Scenario 3 – Lateral Movement

### Hypothesis

The attacker is attempting to move across the network.

### Hunt For

- Multiple RDP logins
- PsExec usage
- SMB connections
- Remote PowerShell
- WMI execution

MITRE ATT&CK

- T1021 – Remote Services

---

# Scenario 4 – Data Exfiltration

### Hypothesis

Sensitive data is leaving the organization.

### Hunt For

- ZIP archive creation
- Dropbox uploads
- Google Drive uploads
- Mega uploads
- Large outbound transfers

MITRE ATT&CK

- T1567 – Exfiltration Over Web Service

---

# Scenario 5 – Persistence

### Hypothesis

The attacker wants to survive reboots.

### Hunt For

- Registry Run Keys
- Scheduled Tasks
- Startup Folder changes
- New Services
- New Local Administrator accounts

MITRE ATT&CK

- T1547
- T1053
- T1136

---

# Hunting Workflow

Every hunt follows the same structure:

Threat Intelligence

↓

Hypothesis

↓

Collect Logs

↓

Analyze Evidence

↓

Validate Findings

↓

Contain Threat

↓

Improve Detection Rules

---

# False Positives During Hunting

Not every suspicious activity is malicious.

Examples:

- IT administrators using PowerShell
- Backup software creating ZIP files
- Developers using remote tools

Threat hunters must always validate findings before escalation.

---

# Documenting a Hunt

Every completed hunt should include:

- Hunt Objective
- Hypothesis
- Logs Reviewed
- Evidence Collected
- MITRE ATT&CK Mapping
- Findings
- Recommendations

Documentation allows hunts to be repeated and improved over time.

---

# Building Hunt Playbooks

Over time, SOC teams build libraries of playbooks.

Examples include:

- PowerShell Hunt Playbook
- Phishing Hunt Playbook
- Credential Dumping Hunt Playbook
- Lateral Movement Hunt Playbook
- Insider Threat Hunt Playbook

These playbooks become part of the organization's detection strategy.

---

# Why This Matters

Threat Hunting is not about waiting for alerts.

It is about actively searching for attacker behaviors before they become incidents.

A skilled threat hunter continuously asks:

> "If I were the attacker, where would I hide?"

---

# Key Takeaways

- Hunt playbooks standardize investigations.
- Every hunt begins with a hypothesis.
- Hunters investigate behaviors, not just alerts.
- MITRE ATT&CK helps map attacker techniques.
- Every completed hunt should improve future detections.
- Documentation is just as important as finding the threat.
