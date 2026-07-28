# Day 61 – Practical Investigation Solutions

## Step 1 – Attack Timeline

| Time | Attacker Activity |
|------|-------------------|
| 08:30 | Attacker researches company employees on LinkedIn |
| 08:40 | Phishing email prepared and sent |
| 08:45 | Employee receives phishing email |
| 08:47 | Employee opens malicious Excel attachment |
| 08:48 | Malicious macro launches PowerShell |
| 08:49 | Malware is downloaded and installed |
| 08:52 | Workstation establishes Command & Control (C2) communication |
| 08:58 | Confidential financial records are stolen |

---

# Step 2 – Cyber Kill Chain Mapping

| Attacker Action | Kill Chain Stage | Explanation |
|-----------------|-----------------|-------------|
| Researching employees | Reconnaissance | Collecting information about potential victims |
| Preparing phishing email | Weaponization | Building the attack payload |
| Sending phishing email | Delivery | Delivering the payload to the victim |
| Opening Excel attachment | Exploitation | Victim triggers malicious code |
| Malware installation | Installation | Malware gains persistence on the system |
| Communication with C2 server | Command & Control | Attacker remotely controls the infected host |
| Stealing financial records | Actions on Objectives | Attacker achieves the intended goal |

---

# Step 3 – MITRE ATT&CK Mapping

| Attacker Action | ATT&CK Tactic | ATT&CK Technique | ATT&CK ID |
|-----------------|---------------|------------------|------------|
| Research employees | Reconnaissance | Gather Victim Identity Information | T1589 |
| Send phishing email | Initial Access | Phishing | T1566 |
| User opens attachment | Execution | User Execution | T1204 |
| PowerShell launched | Execution | PowerShell | T1059.001 |
| Malware downloaded | Command & Control | Ingress Tool Transfer | T1105 |
| Connects to C2 server | Command & Control | Application Layer Protocol | T1071 |
| Steals financial files | Collection | Data from Local System | T1005 |
| Exfiltrates files | Exfiltration | Exfiltration Over Web Service | T1567 |

---

# Step 4 – Framework Comparison

## Cyber Kill Chain

Provides a **high-level view** of the attack.

It answers:

- Where is the attacker in the attack lifecycle?
- What phase has been completed?
- Where can the attack be interrupted?

---

## MITRE ATT&CK

Provides a **detailed technical breakdown**.

It answers:

- What exact technique is being used?
- Which ATT&CK ID matches the activity?
- How can this behavior be detected?
- What defensive controls should be implemented?

---

## Which Provides More Detail?

MITRE ATT&CK.

It breaks attacker actions into individual techniques and maps them to specific IDs, making investigations, threat hunting, and detection engineering much more precise.

---

## Why SOC Teams Use Both

The Cyber Kill Chain provides the **big picture** of an attack.

MITRE ATT&CK explains the **specific behaviors** used at each stage.

Together they give analysts a complete understanding of an incident.

---

# Step 5 – Detection Opportunities

| Detection Point | What Could Be Detected |
|-----------------|------------------------|
| Email Security Gateway | Malicious attachment, suspicious sender, phishing indicators |
| Microsoft Defender | Malicious macro execution and malware download |
| PowerShell Logging | Suspicious PowerShell commands and encoded scripts |
| Sysmon | Process creation, network connections, file creation, PowerShell activity |
| Firewall / Proxy Logs | Outbound communication with the C2 server |
| IDS/IPS | Suspicious traffic patterns and known malicious signatures |
| EDR Platform | Malware execution, persistence, credential theft, lateral movement |
| DLP Solution | Unauthorized transfer of confidential financial documents |

---

# Step 6 – Containment Plan

## Endpoint Actions

- Immediately isolate the infected workstation.
- Stop malicious PowerShell processes.
- Prevent further malware execution.

---

## User Account Actions

- Disable the compromised user account.
- Force an immediate password reset.
- Check for additional compromised accounts.

---

## Network Actions

- Block communication with the Command & Control server.
- Block malicious IP addresses and domains.
- Monitor other endpoints for similar activity.

---

## Evidence Preservation

Collect:

- Windows Event Logs
- Sysmon Logs
- PowerShell Logs
- Memory image
- Network traffic captures
- Malware sample (if safe to collect)

Do **not** wipe the workstation before evidence has been preserved.

---

## Escalation Procedures

- Notify the Incident Response Team.
- Inform management if sensitive financial data has been exposed.
- Begin a full compromise assessment across the environment.

---

# Sample SOC Incident Report

## Incident Summary

A phishing email successfully compromised a Finance employee's workstation. The attacker executed PowerShell, installed malware, established Command & Control communication, and stole confidential financial records.

---

## Root Cause

Successful phishing attack caused by user interaction with a malicious Excel attachment.

---

## Attack Progression

Reconnaissance

↓

Weaponization

↓

Delivery

↓

Exploitation

↓

Installation

↓

Command & Control

↓

Actions on Objectives

---

## MITRE ATT&CK Techniques Observed

| ATT&CK ID | Technique |
|-----------|-----------|
| T1589 | Gather Victim Identity Information |
| T1566 | Phishing |
| T1204 | User Execution |
| T1059.001 | PowerShell |
| T1105 | Ingress Tool Transfer |
| T1071 | Application Layer Protocol |
| T1005 | Data from Local System |
| T1567 | Exfiltration Over Web Service |

---

## Indicators of Compromise (IoCs)

- Suspicious phishing email
- Malicious Excel attachment
- PowerShell execution
- Unknown executable
- Outbound C2 connection
- Unauthorized Dropbox communication
- Access to confidential financial files

---

## Containment Summary

- Workstation isolated
- User account disabled
- Malicious communication blocked
- Evidence preserved
- Incident escalated to Incident Response Team

---

## Lessons Learned

- Strengthen phishing awareness training.
- Block Office macros from untrusted sources.
- Enable enhanced PowerShell logging.
- Improve email filtering.
- Deploy stronger Endpoint Detection and Response (EDR).
- Continuously map detections to MITRE ATT&CK.
- Review DLP policies to reduce the risk of future data exfiltration.

---

# Final Outcome

This investigation demonstrates how the **Cyber Kill Chain** explains the overall progression of an attack, while **MITRE ATT&CK** provides the detailed techniques behind each stage. Using both frameworks together gives SOC analysts a clearer understanding of attacker behavior and improves detection, response, and future defensive planning.
