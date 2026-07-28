# Day 60 – Practical Investigation Solutions

## Step 1 — Attack Timeline

| Time | Attacker Activity |
|------|-------------------|
| 09:15 | Phishing email delivered to employee |
| 09:16 | Employee opened malicious attachment |
| 09:17 | Microsoft Word launched PowerShell |
| 09:18 | PowerShell downloaded a malicious executable |
| 09:20 | LSASS memory was accessed |
| 09:21 | User credentials were dumped |
| 09:24 | Attacker authenticated to another workstation |
| 09:27 | HR documents were compressed into a ZIP archive |
| 09:30 | ZIP archive uploaded to Dropbox |

---

# Step 2 — MITRE ATT&CK Mapping

| Attacker Action | ATT&CK Tactic | ATT&CK Technique | ATT&CK ID |
|-----------------|---------------|------------------|------------|
| Phishing Email | Initial Access | Phishing | T1566 |
| User Opens Attachment | Execution | User Execution | T1204 |
| Word launches PowerShell | Execution | Command and Scripting Interpreter: PowerShell | T1059.001 |
| PowerShell downloads malware | Command & Control | Ingress Tool Transfer | T1105 |
| LSASS accessed | Credential Access | OS Credential Dumping | T1003 |
| Credentials dumped | Credential Access | OS Credential Dumping | T1003 |
| Remote login to another workstation | Lateral Movement | Remote Services | T1021 |
| HR files compressed | Collection | Archive Collected Data | T1560 |
| Files uploaded to Dropbox | Exfiltration | Exfiltration to Cloud Storage | T1567.002 |

---

# Step 3 — Detection Opportunities

A SOC analyst could have detected the attack at several points:

### 1. Email Security Gateway

- Detect malicious attachments.
- Block known phishing domains.
- Sandbox email attachments.

---

### 2. Microsoft Defender / Endpoint Protection

- Detect Microsoft Word spawning PowerShell.
- Alert on suspicious PowerShell commands.

---

### 3. PowerShell Logging

- PowerShell Operational Logs.
- Script Block Logging.
- Encoded PowerShell detection.

---

### 4. Sysmon

Detect:

- PowerShell process creation.
- File downloads.
- LSASS access.
- Process injection.

---

### 5. Windows Event Logs

Monitor:

- Failed logins
- Successful remote logins
- Privilege escalation
- Account changes

---

### 6. Network Monitoring

Detect:

- Dropbox uploads
- Large outbound transfers
- Connections to suspicious IP addresses

---

### 7. EDR Alerts

Detect:

- Credential dumping
- LSASS access
- Lateral movement

---

# Step 4 — Containment Plan

### Immediate Priority

### 1.

Isolate the infected workstation from the network.

---

### 2.

Disable the compromised user's Active Directory account.

---

### 3.

Terminate malicious PowerShell processes.

---

### 4.

Block communication with the malicious IP address and Dropbox destination.

---

### 5.

Reset the compromised user's password.

---

### 6.

Determine whether other endpoints have been affected.

---

### 7.

Preserve forensic evidence.

Do NOT immediately wipe the machine.

Collect:

- Memory image
- Event Logs
- Sysmon Logs
- Network Logs

---

### 8.

Notify the Incident Response Team.

---

# Step 5 — SOC Incident Report

## Incident Summary

A phishing email resulted in malware execution through Microsoft Word and PowerShell. The attacker successfully dumped user credentials, moved laterally to another workstation, compressed HR documents, and exfiltrated them to Dropbox.

---

## Timeline

09:15 – Phishing email delivered

09:16 – Attachment opened

09:17 – Word launched PowerShell

09:18 – Malware downloaded

09:20 – LSASS accessed

09:21 – Credentials dumped

09:24 – Lateral movement detected

09:27 – Files archived

09:30 – Data uploaded to Dropbox

---

## MITRE ATT&CK Mapping

| Technique | ATT&CK ID |
|------------|------------|
| Phishing | T1566 |
| User Execution | T1204 |
| PowerShell | T1059.001 |
| Ingress Tool Transfer | T1105 |
| Credential Dumping | T1003 |
| Remote Services | T1021 |
| Archive Collected Data | T1560 |
| Exfiltration to Cloud Storage | T1567.002 |

---

## Indicators of Compromise (IoCs)

- Malicious email attachment
- Suspicious PowerShell execution
- Unknown executable downloaded
- LSASS memory access
- Remote login from compromised account
- Dropbox outbound connection
- Archived HR documents

---

## Impact Assessment

- User account compromised.
- Sensitive HR documents exposed.
- Lateral movement confirmed.
- Data exfiltration successful.
- High-severity incident requiring full investigation.

---

## Containment Actions

- Endpoint isolated.
- User account disabled.
- Password reset initiated.
- Network communication blocked.
- Evidence preserved.
- Incident escalated.

---

## Lessons Learned

- Strengthen phishing awareness training.
- Enable enhanced PowerShell logging.
- Deploy Sysmon across endpoints.
- Block unauthorized cloud storage services.
- Implement Multi-Factor Authentication (MFA).
- Regularly monitor ATT&CK techniques within SIEM for faster detection.

---

# Final Outcome

The investigation shows that the attacker progressed through multiple stages of the MITRE ATT&CK framework—from **Initial Access** to **Exfiltration**. By mapping each activity to ATT&CK, the SOC team can better understand the attack, improve future detections, and strengthen defensive controls.
