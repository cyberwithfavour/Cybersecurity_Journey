# Day 64 – Threat Hunting Methodology

## Objective

Understand what Threat Hunting is, why organizations perform it, the different hunting methodologies, the hunting lifecycle, and how SOC analysts proactively search for hidden threats that automated tools may miss.

---

# What is Threat Hunting?

Threat Hunting is the **proactive process** of searching for attackers who may already be inside an organization's environment but have not yet been detected by security tools.

Unlike traditional monitoring, Threat Hunting assumes:

> **"The attacker may already be inside."**

Instead of waiting for alerts, hunters actively search for suspicious behavior.

---

# Why is Threat Hunting Important?

Traditional security tools depend on:

- Signatures
- Rules
- Alerts

If an attacker bypasses these controls, they may remain undetected.

Threat Hunting helps organizations:

- Discover hidden attackers
- Reduce dwell time
- Improve detections
- Validate security controls
- Strengthen incident response

---

# What is Dwell Time?

**Dwell Time** is the amount of time an attacker remains inside a network before being discovered.

Example:

Attacker compromises a workstation on Monday.

SOC discovers the attacker on Friday.

Dwell Time = **4 days**

The goal of Threat Hunting is to reduce dwell time as much as possible.

---

# Threat Hunting vs Incident Response

## Threat Hunting

- Proactive
- No confirmed incident
- Searches for hidden threats
- Assumes compromise

---

## Incident Response

- Reactive
- Triggered by alerts
- Responds to confirmed incidents
- Focuses on containment and recovery

---

# Threat Hunting vs Threat Intelligence

Threat Intelligence answers:

> "Who is attacking?"

Threat Hunting answers:

> "Are they already inside our environment?"

Threat Intelligence provides the information.

Threat Hunting searches for evidence.

---

# Threat Hunting Hypothesis

Every hunt begins with a hypothesis.

Example:

> "An attacker may be abusing PowerShell to execute malicious commands."

The hunter then searches logs to prove or disprove the hypothesis.

---

# Threat Hunting Methodologies

## 1. Intelligence-Driven Hunting

Uses:

- Threat Intelligence
- IoCs
- IoAs
- Threat Reports

Example:

Search every endpoint for communication with a known malicious IP.

---

## 2. Hypothesis-Driven Hunting

Begins with an educated assumption.

Example:

"Attackers often dump credentials after phishing."

Search for:

- LSASS access
- Mimikatz activity
- PowerShell execution

---

## 3. Data-Driven Hunting

Starts with unusual activity observed in logs.

Examples:

- Large outbound traffic
- Multiple failed logins
- Rare PowerShell commands

The hunter investigates to determine whether the activity is malicious.

---

# Threat Hunting Lifecycle

## Step 1

Develop a hypothesis.

---

## Step 2

Collect relevant data.

Sources include:

- SIEM
- EDR
- Firewall Logs
- Windows Event Logs
- Sysmon
- DNS Logs

---

## Step 3

Analyze the data.

Look for:

- Abnormal behavior
- MITRE ATT&CK techniques
- Suspicious patterns

---

## Step 4

Investigate findings.

Determine:

- False Positive
- Benign Activity
- Malicious Activity

---

## Step 5

Contain the threat if necessary.

---

## Step 6

Improve detections.

Convert findings into:

- SIEM rules
- EDR detections
- Sigma rules
- Hunting playbooks

---

# Common Threat Hunting Data Sources

- Microsoft Sentinel
- Microsoft Defender for Endpoint
- Windows Event Logs
- Sysmon
- Active Directory Logs
- DNS Logs
- Firewall Logs
- Proxy Logs
- Email Logs
- Cloud Logs

---

# Common Threat Hunting Techniques

Hunters commonly search for:

- PowerShell abuse
- Encoded PowerShell commands
- LSASS access
- Process injection
- Credential dumping
- Lateral movement
- New administrator accounts
- Unusual Remote Desktop activity
- Large outbound data transfers
- Rare parent-child processes

---

# MITRE ATT&CK and Threat Hunting

Threat hunters often build hunts using MITRE ATT&CK.

Example:

Technique:

T1003

Credential Dumping

The hunter searches for:

- LSASS access
- Mimikatz execution
- Security Event Logs
- Defender Alerts

---

# What Makes a Good Threat Hunter?

A good hunter:

- Thinks like an attacker
- Understands Windows internals
- Understands networking
- Knows MITRE ATT&CK
- Understands attacker behavior
- Can analyze logs
- Is curious
- Documents findings clearly

---

# Threat Hunting Workflow

```

Threat Intelligence

↓

Hypothesis

↓

Collect Logs

↓

Analyze Evidence

↓

Investigate

↓

Contain

↓

Improve Detection Rules

```

---

# Real-World Example

Threat Intelligence reports that a ransomware group abuses PowerShell.

Instead of waiting for alerts, the SOC hunts for:

- PowerShell execution
- Encoded commands
- Office applications launching PowerShell
- Network connections after PowerShell execution

The hunt identifies one workstation exhibiting this behavior.

Although no antivirus alert exists, the SOC successfully discovers the attacker before ransomware is deployed.

---

# Why This Matters

Threat Hunting transforms SOC analysts from **reactive defenders** into **proactive defenders**.

Rather than waiting for alerts, hunters actively search for evidence of compromise and continuously improve an organization's security posture.

---

# Key Takeaways

- Threat Hunting is proactive.
- It assumes attackers may already be inside the environment.
- Hunts begin with a hypothesis.
- Hunters use Threat Intelligence, logs, and behavioral analysis.
- The Threat Hunting Lifecycle includes hypothesis, collection, analysis, investigation, containment, and detection improvement.
- MITRE ATT&CK is a core framework used during Threat Hunting.
- Successful Threat Hunting reduces attacker dwell time and strengthens organizational defenses.
