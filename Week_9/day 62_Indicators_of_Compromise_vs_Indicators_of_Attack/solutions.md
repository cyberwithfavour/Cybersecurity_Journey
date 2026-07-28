# Day 62 – Practical Investigation Solutions

## Step 1 – Separate IoCs and IoAs

### Indicators of Compromise (IoCs)

| Indicator | Why it is an IoC |
|-----------|------------------|
| **185.220.101.45** | Known malicious IP address that can be blocked or searched across the environment. |
| **invoice_update.exe** | Malicious executable left behind on the compromised endpoint. |
| **SHA256: 8f7dbe5d8d6c9e5e0a43cdd93e4c2fd10d8bb9c3f2adbaec2f8d1c6a7c18f421** | Unique malware fingerprint used to identify the same file on other systems. |
| **dropbox.com** | Cloud storage service used for data exfiltration in this scenario. |
| **Payroll2026.zip** | Compressed archive created for data theft. |

---

### Indicators of Attack (IoAs)

| Indicator | Why it is an IoA |
|-----------|------------------|
| PowerShell executed with an encoded command | Suspicious attacker behavior often used to evade detection. |
| LSASS memory accessed | Strong indication of credential dumping activity. |
| finance_admin logged into three workstations within five minutes | Indicates possible lateral movement using stolen credentials. |
| ZIP archive created before upload | Common attacker behavior before data exfiltration. |
| File uploaded to Dropbox | Active exfiltration of sensitive information. |

---

# Step 2 – Threat Prioritization

| Finding | Priority | Reason |
|----------|----------|--------|
| LSASS access | **Critical** | Indicates possible credential theft. |
| Lateral movement (finance_admin logins) | **Critical** | Suggests attacker is spreading across the environment. |
| Data upload to Dropbox | **Critical** | Sensitive data is leaving the organization. |
| Encoded PowerShell | **High** | Strong indication of malicious execution. |
| Malware download | **High** | Endpoint compromise confirmed. |
| Malicious IP connection | **High** | Active communication with attacker infrastructure. |
| ZIP archive creation | **Medium** | Suspicious but becomes critical when combined with exfiltration. |

---

# Step 3 – Investigation Timeline

| Time | Event |
|------|-------|
| 09:10 | PowerShell launched with encoded command |
| 09:11 | Malware downloaded from external server |
| 09:12 | Connection established to 185.220.101.45 |
| 09:14 | LSASS process accessed |
| 09:16 | Credentials stolen |
| 09:18 | finance_admin authenticated to multiple workstations |
| 09:22 | Payroll2026.zip created |
| 09:24 | ZIP archive uploaded to Dropbox |

---

# Step 4 – Containment Plan

## Endpoint Actions

- Immediately isolate the infected workstation.
- Stop malicious PowerShell processes.
- Quarantine the downloaded executable.

---

## User Account Actions

- Disable **finance_admin**.
- Force password reset.
- Review privileged accounts for suspicious activity.

---

## Network Actions

- Block **185.220.101.45**.
- Block outbound communication to Dropbox until investigation is complete.
- Search for other devices communicating with the same IP.

---

## Evidence Preservation

Collect:

- Windows Event Logs
- PowerShell Logs
- Sysmon Logs
- Memory dump
- Network traffic
- Malware sample

---

## Escalation

- Notify Incident Response Team.
- Inform SOC Manager.
- Escalate to management due to potential data loss.

---

# Step 5 – Threat Intelligence

Immediately search across the environment for:

| IoC | Reason |
|------|--------|
| 185.220.101.45 | Identify other compromised hosts communicating with the attacker. |
| SHA256 hash | Locate the same malware on other endpoints. |
| invoice_update.exe | Detect additional infected systems. |
| dropbox.com activity | Identify possible data exfiltration from other devices. |
| Payroll2026.zip | Determine whether similar archives exist elsewhere. |

---

# Step 6 – Detection Improvements

Implement detections for:

1. Microsoft Office spawning PowerShell.
2. Encoded PowerShell commands.
3. LSASS memory access.
4. Multiple workstation logins by the same account within a short period.
5. Large outbound uploads to cloud storage providers.
6. Creation of ZIP archives containing sensitive documents.
7. Endpoint communication with known malicious IP addresses.
8. Malware downloads from suspicious domains.

---

# Step 7 – SOC Incident Report

## Incident Summary

Microsoft Defender detected suspicious PowerShell execution that led to malware download, credential dumping, lateral movement, and successful data exfiltration to Dropbox.

---

## Timeline

- Encoded PowerShell executed
- Malware downloaded
- Connection established to malicious IP
- LSASS accessed
- Credentials stolen
- Lateral movement observed
- Sensitive files compressed
- Data exfiltrated

---

## Indicators of Compromise (IoCs)

- Malicious IP: **185.220.101.45**
- File: **invoice_update.exe**
- SHA256 hash
- Dropbox communication
- Payroll2026.zip

---

## Indicators of Attack (IoAs)

- Encoded PowerShell
- LSASS access
- Credential dumping
- Lateral movement
- Data exfiltration behavior

---

## Risk Assessment

**Severity:** Critical

The attacker successfully compromised credentials, moved laterally, and exfiltrated sensitive payroll information. Immediate containment and a full enterprise-wide investigation are required.

---

## Containment Actions

- Endpoint isolated
- User account disabled
- Malicious IP blocked
- Evidence preserved
- Incident escalated to Incident Response

---

## Recommended Improvements

- Enable enhanced PowerShell logging.
- Deploy Sysmon across all endpoints.
- Strengthen EDR behavioral detections.
- Restrict unauthorized cloud storage usage.
- Enforce Multi-Factor Authentication (MFA).
- Monitor privileged account activity continuously.
- Conduct phishing awareness training.

---

# Final Outcome

This investigation demonstrates the importance of combining **Indicators of Compromise (IoCs)** with **Indicators of Attack (IoAs)**. IoCs help identify known malicious artifacts, while IoAs expose attacker behavior in real time. Modern SOC analysts rely on both to detect, investigate, contain, and prevent cyber threats effectively.
