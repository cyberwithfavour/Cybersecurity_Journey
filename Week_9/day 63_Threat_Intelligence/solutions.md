# Day 63 – Practical Investigation Solutions

## Step 1 – Threat Intelligence Validation

### Intelligence Correlation

| SIEM Finding | Matches Threat Intelligence? | Assessment |
|--------------|----------------------------|------------|
| Connection to **185.220.101.45** | ✅ Yes | Confirmed communication with a known malicious Command & Control (C2) server. |
| Two users visited **secure-update365.com** | ✅ Yes | Users accessed a known malicious phishing domain. Immediate investigation required. |
| SHA256 hash detected on endpoint | ✅ Yes | Malware associated with the campaign has been found. Endpoint is compromised. |
| Microsoft Word launched PowerShell | ✅ Yes | Matches the threat actor's execution technique. Strong IoA. |
| Dropbox uploads from Finance | ⚠️ Likely | Consistent with the threat actor's data exfiltration behavior. Requires investigation. |

---

### Systems Likely Compromised

- Finance-PC-04
- Finance-PC-07
- Laptop assigned to Finance Manager

These systems should be treated as compromised until proven otherwise.

---

# Step 2 – Threat Actor Profile

| Field | Information |
|--------|-------------|
| Threat Actor | APT-Shadow |
| Campaign | Operation Silent Invoice |
| Risk Level | Critical |
| Likely Targets | Finance departments, accounting teams, organizations handling financial transactions |
| Primary Objective | Credential theft and financial data exfiltration |
| Common TTPs | Spear Phishing, PowerShell execution, Credential Dumping, Remote Services, Cloud Storage Exfiltration |

---

# Step 3 – IOC Watchlist

## Malicious IP Addresses

- 185.220.101.45
- 91.214.124.77

---

## Malicious Domains

- secure-update365.com
- microsoft-login365.net

---

## File Hash

```
SHA256

8f7dbe5d8d6c9e5e0a43cdd93e4c2fd10d8bb9c3f2adbaec2f8d1c6a7c18f421
```

---

## Suspicious Behaviors (IoAs)

- Microsoft Office spawning PowerShell
- Encoded PowerShell commands
- LSASS memory access
- Credential dumping
- Remote authentication to multiple hosts
- ZIP archive creation before outbound transfer
- Dropbox uploads from corporate devices

---

# Step 4 – Threat Hunt

The SOC should immediately perform the following hunts:

### Hunt 1

Search firewall and proxy logs for communication with:

- 185.220.101.45
- 91.214.124.77

---

### Hunt 2

Search DNS logs for:

- secure-update365.com
- microsoft-login365.net

---

### Hunt 3

Search all endpoints for the SHA256 malware hash.

---

### Hunt 4

Search PowerShell Operational Logs for:

- Encoded commands
- Download activity
- Suspicious execution

---

### Hunt 5

Search EDR telemetry for:

- LSASS access
- Credential dumping
- Process injection

---

### Hunt 6

Review outbound traffic for:

- Dropbox
- OneDrive
- Google Drive
- Mega
- Other cloud storage providers

---

# Step 5 – Immediate Response

## Network Actions

- Block malicious IP addresses.
- Block malicious domains.
- Block outbound Dropbox communication until investigation is complete.

---

## Endpoint Actions

- Isolate compromised devices.
- Quarantine malware.
- Collect forensic evidence before remediation.

---

## User Actions

- Disable affected accounts.
- Force password resets.
- Review privileged accounts for suspicious activity.

---

## Investigation Actions

- Preserve logs.
- Collect memory images.
- Capture network traffic.
- Notify the Incident Response Team.

---

## Escalation

Escalate immediately because:

- Active malware is present.
- Credential theft has occurred.
- Potential data exfiltration has been detected.

---

# Step 6 – Threat Intelligence Report

## Executive Summary

Threat Intelligence identified an active campaign known as **Operation Silent Invoice** conducted by **APT-Shadow**. SIEM telemetry confirms multiple matches between organizational activity and known campaign indicators.

---

## Threat Actor Overview

APT-Shadow is a financially motivated threat group known for phishing campaigns targeting finance departments. The group uses PowerShell-based malware, credential dumping, lateral movement, and cloud storage services for data exfiltration.

---

## Campaign Description

The campaign begins with spear-phishing emails containing malicious Office documents. Once opened, PowerShell downloads malware, credentials are harvested, lateral movement is performed, and sensitive financial data is uploaded to cloud storage.

---

## Indicators of Compromise

### IP Addresses

- 185.220.101.45
- 91.214.124.77

### Domains

- secure-update365.com
- microsoft-login365.net

### File Hash

- SHA256:
  `8f7dbe5d8d6c9e5e0a43cdd93e4c2fd10d8bb9c3f2adbaec2f8d1c6a7c18f421`

---

## MITRE ATT&CK Techniques Observed

| Technique | ATT&CK ID |
|-----------|-----------|
| Phishing | T1566 |
| User Execution | T1204 |
| PowerShell | T1059.001 |
| Ingress Tool Transfer | T1105 |
| Credential Dumping | T1003 |
| Remote Services | T1021 |
| Exfiltration to Cloud Storage | T1567.002 |

---

## Systems Affected

- Finance-PC-04
- Finance-PC-07
- Finance Manager Laptop

---

## Risk Assessment

**Overall Severity:** Critical

Evidence indicates successful phishing, malware execution, credential compromise, and probable data exfiltration. Immediate containment and organization-wide hunting are required.

---

## Recommended Defensive Actions

- Block all identified IoCs.
- Deploy updated EDR detection rules.
- Hunt across all endpoints for campaign indicators.
- Enforce Multi-Factor Authentication (MFA).
- Disable Office macros from untrusted sources.
- Enable enhanced PowerShell logging.
- Increase user awareness through phishing simulations.
- Map all future detections to the MITRE ATT&CK Framework.

---

# Final Outcome

This investigation demonstrates how Threat Intelligence transforms isolated alerts into a complete understanding of an attack campaign. By correlating intelligence feeds with SIEM data, the SOC can quickly identify compromised systems, understand the attacker's methods, contain the threat, and strengthen future defenses.
