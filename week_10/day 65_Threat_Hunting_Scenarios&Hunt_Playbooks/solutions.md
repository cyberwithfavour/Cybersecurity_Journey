# Day 65 – Practical Investigation Solutions

## Step 1 – Hunt Playbooks Used

| Hunt Playbook | Why It Was Selected |
|---------------|---------------------|
| **PowerShell Abuse** | Microsoft Word launched PowerShell and downloaded a script. |
| **Persistence** | A new local administrator account (`backup_admin`) was created. |
| **Lateral Movement** | The new account logged into multiple file servers. |
| **Data Exfiltration** | A ZIP archive was uploaded to Mega.nz. |
| **Credential Theft** | The attacker likely created the admin account after obtaining elevated privileges. This requires further investigation. |

---

# Step 2 – Hunting Hypotheses

### Hypothesis 1 – PowerShell Abuse

An attacker may be using Microsoft Office to execute malicious PowerShell commands and download malware.

---

### Hypothesis 2 – Persistence

The attacker may have created a local administrator account to maintain long-term access.

---

### Hypothesis 3 – Lateral Movement

The attacker may be using the newly created administrator account to move across multiple servers.

---

### Hypothesis 4 – Data Exfiltration

The attacker may be compressing sensitive files and uploading them to cloud storage.

---

### Hypothesis 5 – Credential Theft

The attacker may have obtained administrative credentials before creating the new account.

---

# Step 3 – Evidence Collection

| Hunt | Evidence Found | Additional Evidence Needed | Data Source |
|------|----------------|----------------------------|-------------|
| PowerShell Abuse | Word launched PowerShell | Full PowerShell command line | Sysmon, PowerShell Logs |
| Persistence | New admin account created | Who created the account | Windows Security Logs, Active Directory |
| Lateral Movement | Login to two file servers | Authentication history | AD Logs, Event ID 4624 |
| Data Exfiltration | ZIP uploaded to Mega | File contents, upload size | Proxy Logs, Firewall Logs |
| Credential Theft | Privileged account activity | LSASS access, Defender alerts | Defender, Sysmon |

---

# Step 4 – Investigation Timeline

| Time | Event |
|------|-------|
| 09:02 | User opens Microsoft Word document |
| 09:03 | Word launches PowerShell |
| 09:04 | PowerShell downloads `update.ps1` |
| 09:06 | Attacker gains code execution |
| 09:08 | Local administrator account `backup_admin` created |
| 09:12 | `backup_admin` logs into File Server 1 |
| 09:15 | `backup_admin` logs into File Server 2 |
| 09:20 | `Finance_Backup.zip` created |
| 09:25 | ZIP uploaded to Mega.nz |

---

# Step 5 – MITRE ATT&CK Mapping

| Activity | ATT&CK Tactic | ATT&CK Technique | ATT&CK ID |
|----------|---------------|------------------|-----------|
| Word launches PowerShell | Execution | PowerShell | **T1059.001** |
| PowerShell downloads script | Command & Control | Ingress Tool Transfer | **T1105** |
| Local admin account created | Persistence | Create Account | **T1136** |
| Login to multiple servers | Lateral Movement | Remote Services | **T1021** |
| ZIP archive created | Collection | Archive Collected Data | **T1560** |
| Upload to Mega.nz | Exfiltration | Exfiltration Over Web Service | **T1567.002** |

---

# Step 6 – Attack Stage Assessment

## Persistence

**Status:** Confirmed ✅

**Evidence**

- New administrator account (`backup_admin`) was created.

---

## Lateral Movement

**Status:** Confirmed ✅

**Evidence**

- The account authenticated to multiple file servers within minutes.

---

## Credential Theft

**Status:** Suspected ⚠️

**Evidence**

- Administrative actions occurred.
- No direct evidence of LSASS access or credential dumping was observed.
- Additional investigation is required.

---

## Data Exfiltration

**Status:** Confirmed ✅

**Evidence**

- `Finance_Backup.zip` was uploaded to Mega.nz.

---

# Step 7 – Detection Engineering Recommendations

The SOC should implement the following detection rules:

1. Alert when Microsoft Office launches PowerShell.
2. Alert when PowerShell downloads files from external URLs.
3. Alert when encoded PowerShell commands are executed.
4. Alert when new local administrator accounts are created.
5. Alert when newly created administrator accounts authenticate to multiple systems within a short period.
6. Alert when ZIP archives are created inside sensitive folders.
7. Alert when corporate devices upload files to Mega, Dropbox, Google Drive, or similar cloud services.
8. Alert when PowerShell is executed with the `ExecutionPolicy Bypass` parameter.

---

# Step 8 – Threat Hunting Report

## Executive Summary

A proactive threat hunt uncovered evidence of an active compromise involving PowerShell abuse, persistence, lateral movement, and successful data exfiltration.

---

## Hunt Playbooks Used

- PowerShell Abuse
- Persistence
- Lateral Movement
- Data Exfiltration
- Credential Theft

---

## Hunting Hypotheses

- Office documents may be executing malicious PowerShell.
- An attacker may have established persistence using a new administrator account.
- The attacker may be moving laterally across file servers.
- Sensitive financial files may be leaving the organization.

---

## Evidence Collected

- Microsoft Word launched PowerShell.
- PowerShell downloaded a remote script.
- Local administrator account created.
- Administrator account logged into multiple servers.
- ZIP archive created.
- ZIP uploaded to Mega.nz.

---

## MITRE ATT&CK Techniques

| ATT&CK ID | Technique |
|-----------|-----------|
| T1059.001 | PowerShell |
| T1105 | Ingress Tool Transfer |
| T1136 | Create Account |
| T1021 | Remote Services |
| T1560 | Archive Collected Data |
| T1567.002 | Exfiltration Over Web Service |

---

## Investigation Timeline

1. Office document opened.
2. PowerShell executed.
3. Malicious script downloaded.
4. Persistence established.
5. Lateral movement performed.
6. Financial files compressed.
7. Data uploaded to Mega.nz.

---

## Findings

The threat hunt confirmed that multiple stages of the Cyber Kill Chain were completed successfully. Although no malware alert was generated, behavioral evidence clearly indicates an active compromise.

---

## Risk Assessment

**Severity:** Critical

The attacker achieved:

- Code execution
- Persistence
- Lateral movement
- Data exfiltration

Immediate Incident Response actions are required.

---

## Recommended Detection Improvements

- Strengthen PowerShell monitoring.
- Deploy Sysmon on all endpoints.
- Restrict Office child processes.
- Monitor administrator account creation.
- Block unauthorized cloud storage services.
- Monitor archive creation in sensitive directories.
- Enable enhanced Defender behavioral detections.
- Continuously update hunt playbooks using MITRE ATT&CK.

---

## Final Conclusion

This investigation highlights why **Threat Hunting is essential**. No high-severity alerts were triggered, yet the hunt revealed a sophisticated attack in progress. By following structured hunt playbooks and correlating multiple low-level events, the SOC successfully identified attacker activity before additional damage occurred.
