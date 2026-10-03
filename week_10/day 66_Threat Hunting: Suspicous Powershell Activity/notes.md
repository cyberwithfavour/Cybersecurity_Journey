# Day 66 — Threat Hunting: Suspicious PowerShell Activity

## 1. Introduction

PowerShell is a powerful Windows command-line shell and scripting language used for system administration and automation.

Because PowerShell can perform many powerful actions on a Windows system, attackers may also abuse it after gaining access to an endpoint.

As a SOC Analyst, the goal is not to treat every PowerShell event as malicious.

The goal is to investigate the activity, understand the context, correlate evidence, and determine whether the behavior is:

* Benign
* Suspicious
* Potentially malicious

---

## 2. What is PowerShell?

PowerShell is a command-line shell and scripting language developed for Windows administration and automation.

Administrators can use PowerShell to:

* Manage users
* Manage processes
* Manage services
* Configure systems
* Automate tasks
* Query system information
* Execute scripts
* Manage network resources

### Example

```powershell
Get-Process
```

This command displays running processes.

Another example:

```powershell
Get-Service
```

This command displays services running on a Windows system.

PowerShell itself is legitimate.

The security concern is **how it is being used**.

---

## 3. Why is PowerShell Important to a SOC Analyst?

Attackers may abuse PowerShell to:

* Execute commands
* Run scripts
* Download files
* Execute malicious code
* Perform reconnaissance
* Collect information
* Attempt credential access
* Establish persistence
* Communicate with remote systems

This makes PowerShell an important source of evidence during endpoint investigations and threat hunting.

---

## 4. Legitimate vs Suspicious PowerShell

PowerShell can be used by:

### Legitimate users

For example:

```text
System Administrator
        ↓
PowerShell
        ↓
System maintenance
```

### Potentially malicious users

For example:

```text
Compromised Account
        ↓
PowerShell
        ↓
Encoded Command
        ↓
External Connection
```

The second example contains several indicators that deserve investigation.

However, even suspicious characteristics must be investigated in context.

---

# 5. What is Threat Hunting?

Threat hunting is a proactive security activity where an analyst searches an environment for evidence of threats that may not have been detected automatically.

A basic threat-hunting process is:

```text
Hunting Hypothesis
        ↓
Data Sources
        ↓
Search
        ↓
Investigation
        ↓
Correlation
        ↓
Findings
        ↓
Conclusion
```

---

# 6. Threat Hunting Hypothesis

A hunting hypothesis gives the investigation a specific question to investigate.

### PowerShell Hunting Hypothesis

> An attacker may use PowerShell to execute commands on an endpoint after gaining unauthorized access.

The analyst then searches available security data for evidence that supports or disproves the hypothesis.

---

# 7. What Makes PowerShell Activity Suspicious?

Some characteristics that may require investigation include:

* Encoded commands
* Obfuscated commands
* Unusual parent processes
* Unexpected scripts
* PowerShell launched by Microsoft Office applications
* Commands that download files
* Commands that execute files
* Unexpected external connections
* PowerShell activity from unusual accounts
* Activity occurring at unusual times
* PowerShell execution on systems where it is not normally required

No single indicator automatically proves compromise.

The analyst should correlate multiple indicators.

---

# 8. Parent-Child Process Relationships

A process relationship shows which process started another process.

For example:

```text
WINWORD.EXE
     ↓
powershell.exe
     ↓
script
```

The parent process is:

```text
WINWORD.EXE
```

The child process is:

```text
powershell.exe
```

Understanding this relationship can help the analyst determine how PowerShell was launched.

---

# 9. Encoded PowerShell

Attackers may encode PowerShell commands to make the command harder to understand or detect.

Example:

```powershell
powershell.exe -EncodedCommand [encoded content]
```

When this appears during an investigation, the analyst should determine:

* What does the command contain?
* What does it attempt to execute?
* Does it download anything?
* Does it communicate externally?
* Does it create persistence?
* Does it collect information?

Encoded PowerShell is an investigation indicator, not automatic proof of malicious activity.

---

# 10. Evidence Sources

A SOC Analyst may use several sources to investigate PowerShell activity.

### Endpoint Data

* Windows Event Logs
* PowerShell logs
* Sysmon
* EDR telemetry

### Network Data

* DNS logs
* Proxy logs
* Firewall logs
* Network connection logs

### Security Data

* SIEM
* Authentication logs
* Threat intelligence
* Security alerts

Correlating these sources can provide a more complete picture.

---

# 11. Important Investigation Fields

| Field          | Question                                 |
| -------------- | ---------------------------------------- |
| Username       | Who executed PowerShell?                 |
| Hostname       | Which endpoint was involved?             |
| Timestamp      | When did it happen?                      |
| Process        | What process was executed?               |
| Parent Process | What launched PowerShell?                |
| Command        | What was executed?                       |
| Script         | Was a script involved?                   |
| Destination    | Did the endpoint communicate externally? |
| IP/Domain      | Where did it communicate?                |
| User Context   | Was the activity expected?               |

---

# 12. Investigation Methodology

## Step 1 — Identify the User

Determine the account associated with the activity.

Ask:

* Is the account legitimate?
* Is the user expected to use PowerShell?
* Was the user working at the time?
* Does the user's role require administrative activity?

---

## Step 2 — Identify the Endpoint

Determine which machine generated the event.

Record:

```text
Hostname:
IP Address:
User:
Operating System:
Department:
```

This establishes the environment and user context.

---

## Step 3 — Examine the PowerShell Command

Review the command or script.

Look for:

* Encoded commands
* Obfuscation
* File downloads
* Script execution
* System discovery
* Credential-related activity
* Remote connections

---

## Step 4 — Examine the Parent Process

Determine which process launched PowerShell.

For example:

```text
explorer.exe → powershell.exe
```

or:

```text
winword.exe → powershell.exe
```

The second relationship may require additional investigation depending on the context.

---

## Step 5 — Review Network Activity

Determine whether PowerShell communicated with external systems.

Look for:

* IP addresses
* Domains
* DNS queries
* HTTP/HTTPS connections
* Unusual destinations
* Connections immediately after PowerShell execution

---

## Step 6 — Correlate the Evidence

Do not investigate each event independently.

Correlate:

```text
User
 ↓
Endpoint
 ↓
Process
 ↓
Command
 ↓
Network Activity
 ↓
Destination
 ↓
Context
```

This helps determine what actually happened.

---

# 13. Classification

After investigating the available evidence, the activity can be classified.

### Benign

The activity has a legitimate explanation and supporting evidence.

### Suspicious

The activity contains unusual characteristics, but there is not enough evidence to confirm malicious behavior.

### Potentially Malicious

Multiple indicators suggest unauthorized or malicious activity and further response or escalation is required.

---

# 14. MITRE ATT&CK Mapping

### T1059.001 — Command and Scripting Interpreter: PowerShell

PowerShell is mapped to the MITRE ATT&CK technique:

**T1059.001 — PowerShell**

This technique describes the use of PowerShell for command and scripting execution.

The mapping should be supported by the evidence discovered during the investigation.

---

# 15. Detection Improvements

A SOC can improve PowerShell detection by monitoring:

* PowerShell execution
* Encoded commands
* Script Block Logging
* Suspicious parent-child process relationships
* PowerShell network connections
* Unusual PowerShell users
* PowerShell activity across endpoints
* EDR telemetry

Detection rules should focus on **suspicious behavior**, rather than simply alerting on every PowerShell event.

---

# 16. Incident Response Considerations

If malicious activity is confirmed, the SOC may:

1. Preserve evidence.
2. Identify the affected endpoint.
3. Identify the account involved.
4. Investigate the command or script.
5. Review authentication activity.
6. Investigate network connections.
7. Search for related activity on other endpoints.
8. Escalate the incident.
9. Contain the affected endpoint or account when appropriate.
10. Document the investigation.

---

# 17. Key Takeaways

* PowerShell is a legitimate administration tool.
* Attackers can abuse PowerShell.
* PowerShell execution alone does not prove compromise.
* Threat hunting begins with a hypothesis.
* Parent-child process relationships provide useful context.
* Encoded commands deserve investigation.
* Network activity can provide additional evidence.
* Multiple indicators should be correlated.
* MITRE ATT&CK T1059.001 represents PowerShell.
* SOC Analysts should make evidence-based conclusions.

---

# Analyst Rule to Remember

> **Do not hunt for PowerShell. Hunt for suspicious PowerShell behavior.**

A useful investigation mindset is:

```text
WHO?
 ↓
WHAT?
 ↓
WHERE?
 ↓
WHEN?
 ↓
HOW?
 ↓
WHY?
 ↓
WHAT HAPPENED NEXT?
```

---

## Day 66 Summary

**Topic:** Threat Hunting — Suspicious PowerShell Activity

**Focus Area:** Threat Hunting / SOC Analysis

**MITRE ATT&CK:** T1059.001 — PowerShell

**Investigation Type:** Endpoint Threat Hunting

**Day:** 66
