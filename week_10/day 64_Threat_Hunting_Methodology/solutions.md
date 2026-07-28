# Day 64 – Practical Investigation Solutions

## Step 1 – Hunting Hypothesis

### Hypothesis

A ransomware group may have already compromised one or more endpoints by abusing Microsoft Office to execute PowerShell commands. The attacker may be attempting credential dumping and lateral movement before deploying ransomware.

### Why?

Recent Threat Intelligence reports indicate that this threat actor consistently uses:

- Spear phishing
- PowerShell execution
- Credential dumping
- Lateral movement

before encrypting systems.

### High-Risk Systems

- Finance Department
- Human Resources
- Domain Controllers
- Executive Laptops
- File Servers

---

# Step 2 – Data Sources

| Data Source | Purpose |
|-------------|----------|
| Microsoft Sentinel | Correlate logs and identify suspicious activities across the environment. |
| Microsoft Defender for Endpoint | Detect malicious processes, malware, and endpoint behaviors. |
| Sysmon | Monitor process creation, PowerShell activity, network connections, and file creation. |
| Windows Security Event Logs | Review logon events, privilege changes, and account activity. |
| Active Directory Logs | Detect new accounts, privilege escalation, and abnormal authentication. |
| DNS Logs | Identify communication with suspicious domains. |
| Firewall Logs | Detect outbound communication to malicious IP addresses. |
| Proxy Logs | Review internet browsing activity and file downloads. |

---

# Step 3 – Hunt Findings

| Suspicious Activity | Status | Reason |
|---------------------|--------|--------|
| Microsoft Word launched PowerShell | Suspicious | Office applications rarely need to launch PowerShell. |
| Encoded PowerShell command detected | Suspicious | Common attacker obfuscation technique. |
| PowerShell downloaded an executable | Malicious | Indicates possible malware delivery. |
| LSASS accessed by PowerShell | Malicious | Strong indication of credential dumping. |
| finance_admin logged into three systems within five minutes | Suspicious | Possible lateral movement. |
| Large outbound traffic to cloud storage | Suspicious | Possible data exfiltration. |
| New administrator account created outside business hours | Suspicious | Possible persistence or privilege escalation. |

---

# Step 4 – MITRE ATT&CK Mapping

| Suspicious Activity | ATT&CK Tactic | ATT&CK Technique | ATT&CK ID |
|---------------------|---------------|------------------|------------|
| Office launching PowerShell | Execution | PowerShell | T1059.001 |
| Encoded PowerShell | Defense Evasion | Obfuscated Files or Information | T1027 |
| PowerShell downloading malware | Command & Control | Ingress Tool Transfer | T1105 |
| LSASS access | Credential Access | OS Credential Dumping | T1003 |
| Multiple workstation logins | Lateral Movement | Remote Services | T1021 |
| Large outbound upload | Exfiltration | Exfiltration Over Web Service | T1567 |
| New administrator account | Persistence | Create Account | T1136 |

---

# Step 5 – Hunt Conclusion

### Investigation Result

**Active compromise confirmed.**

### Evidence

- Microsoft Office executed PowerShell.
- Encoded PowerShell commands were observed.
- Malware was downloaded.
- LSASS memory was accessed.
- Multiple workstations were accessed using the same account.
- Large outbound uploads were detected.

These findings strongly indicate attacker activity rather than normal administrative behavior.

---

# Step 6 – Detection Improvements

The SOC should implement the following detection rules:

1. Alert when Microsoft Office applications spawn PowerShell.
2. Alert on Base64-encoded PowerShell commands.
3. Alert when PowerShell downloads executable files from the internet.
4. Alert when any non-system process accesses `lsass.exe`.
5. Alert when a privileged account logs into multiple endpoints within a short period.
6. Alert when ZIP archives containing sensitive files are created.
7. Alert on unusually large outbound uploads to cloud storage providers.
8. Alert when administrator accounts are created outside approved maintenance windows.

---

# Step 7 – Threat Hunting Report

## Hunt Objective

Determine whether the ransomware group's known behaviors are present within the organization's environment before any security alert is triggered.

---

## Hunting Hypothesis

An attacker may already have compromised one or more endpoints using phishing and PowerShell, and may currently be attempting credential theft and lateral movement.

---

## Data Sources Used

- Microsoft Sentinel
- Microsoft Defender for Endpoint
- Sysmon
- Windows Event Logs
- Active Directory Logs
- DNS Logs
- Firewall Logs
- Proxy Logs

---

## MITRE ATT&CK Techniques Observed

| ATT&CK ID | Technique |
|-----------|-----------|
| T1059.001 | PowerShell |
| T1027 | Obfuscated Files or Information |
| T1105 | Ingress Tool Transfer |
| T1003 | OS Credential Dumping |
| T1021 | Remote Services |
| T1567 | Exfiltration Over Web Service |
| T1136 | Create Account |

---

## Findings

The hunt identified multiple attacker behaviors that align with the ransomware group's known TTPs.

Observed behaviors include:

- Office spawning PowerShell
- Encoded PowerShell execution
- Malware download
- Credential dumping
- Lateral movement
- Suspicious outbound traffic

---

## Evidence Collected

- PowerShell Operational Logs
- Sysmon Process Creation Logs
- Windows Security Logs
- Defender Alerts
- Firewall Traffic Logs
- Active Directory Authentication Logs

---

## Risk Assessment

**Severity:** Critical

The combination of PowerShell abuse, credential dumping, and lateral movement strongly suggests that an attacker is actively operating inside the environment.

Immediate containment and a full Incident Response process are required.

---

## Recommended Detection Improvements

- Enable Script Block Logging.
- Deploy Sysmon to all endpoints.
- Block Microsoft Office from launching child processes where possible.
- Monitor LSASS access continuously.
- Enable alerts for unusual authentication patterns.
- Monitor cloud storage usage for unauthorized uploads.
- Continuously map detections to MITRE ATT&CK techniques.

---

## Final Conclusion

This proactive threat hunt successfully identified attacker behaviors **before ransomware deployment**. Instead of waiting for automated alerts, the SOC used hypothesis-driven hunting, log analysis, and MITRE ATT&CK mapping to uncover an active compromise, demonstrating the value of proactive defense in modern Security Operations Centers.
