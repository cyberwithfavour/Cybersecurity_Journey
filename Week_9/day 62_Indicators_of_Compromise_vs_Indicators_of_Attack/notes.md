# Day 62 – Indicators of Compromise (IoCs) vs Indicators of Attack (IoAs)

## Objective

Understand the difference between Indicators of Compromise (IoCs) and Indicators of Attack (IoAs), how they are used during incident investigations, and why modern SOCs increasingly rely on behavioral detection.

---

# What are Indicators of Compromise (IoCs)?

Indicators of Compromise (IoCs) are **pieces of forensic evidence** that suggest a system **has already been compromised**.

Think of IoCs as the **digital fingerprints** left behind by an attacker.

They help security teams answer the question:

> "Has this system already been attacked?"

---

# Examples of IoCs

Common IoCs include:

- Malicious IP addresses
- Malicious domains
- Suspicious URLs
- File hashes (MD5, SHA-1, SHA-256)
- Malware file names
- Registry modifications
- Email addresses
- Command & Control (C2) servers
- Suspicious scheduled tasks

Example:

```
185.220.101.5
```

If this IP is known to host malware, it becomes an IoC.

---

# What are Indicators of Attack (IoAs)?

Indicators of Attack (IoAs) are **behaviors** that suggest an attacker is actively attempting to compromise a system.

Instead of looking for known malicious files or IP addresses, IoAs focus on **what the attacker is doing**.

They answer the question:

> "Is an attack happening right now?"

---

# Examples of IoAs

Common IoAs include:

- Microsoft Word launching PowerShell
- PowerShell downloading files
- LSASS memory access
- Process injection
- Credential dumping
- Privilege escalation
- Lateral movement
- Unusual parent-child processes
- Suspicious remote logins
- Ransomware encrypting files

Example:

```
WINWORD.exe
        ↓
powershell.exe
```

This behavior is highly suspicious, even if the PowerShell script has never been seen before.

---

# IoCs vs IoAs

| Indicators of Compromise (IoCs) | Indicators of Attack (IoAs) |
|---------------------------------|-----------------------------|
| Evidence of a past compromise | Evidence of active attacker behavior |
| Reactive | Proactive |
| Signature-based | Behavior-based |
| Easy for attackers to change | Much harder for attackers to change |
| Useful after compromise | Useful during an attack |

---

# Types of IoCs

## Network IoCs

- Malicious IP addresses
- Malicious domains
- Suspicious DNS requests
- Suspicious URLs

---

## Host IoCs

- Malware file names
- File hashes
- Registry changes
- New services
- Suspicious scheduled tasks

---

## Email IoCs

- Malicious sender addresses
- Phishing domains
- Suspicious attachments

---

## User IoCs

- Compromised accounts
- Multiple failed logins
- Impossible travel logins

---

# Types of IoAs

## Execution Behaviors

- PowerShell abuse
- CMD abuse
- WMI execution
- Office spawning scripts

---

## Credential Behaviors

- LSASS access
- Mimikatz activity
- Token manipulation

---

## Persistence Behaviors

- New scheduled tasks
- Startup folder changes
- Registry Run Keys

---

## Lateral Movement Behaviors

- PsExec
- Remote Desktop abuse
- SMB connections
- WMI remote execution

---

## Data Theft Behaviors

- Large file compression
- Cloud storage uploads
- Mass file access

---

# Why IoAs Are Becoming More Important

Attackers constantly change:

- Malware names
- IP addresses
- Domains
- File hashes

This makes IoCs less reliable over time.

However, attackers still need to:

- Execute code
- Dump credentials
- Move laterally
- Communicate with C2 servers

These behaviors are much harder to hide.

---

# Behavioral Detection

Behavioral detection focuses on **how** a process behaves rather than **what** it is.

Example:

Instead of asking:

> Is this malware?

It asks:

> Why is Microsoft Word launching PowerShell?

This is the foundation of modern Endpoint Detection and Response (EDR).

---

# Signature-Based Detection

Traditional antivirus relies on signatures.

It compares files against known malware.

Advantages:

- Fast
- Accurate for known threats

Disadvantages:

- Cannot detect brand-new malware
- Easily bypassed

---

# Behavioral Detection

Modern EDR solutions monitor behaviors.

Advantages:

- Detects unknown malware
- Detects fileless attacks
- Detects living-off-the-land techniques

Examples include:

- Microsoft Defender for Endpoint
- CrowdStrike Falcon
- SentinelOne
- Sophos Intercept X

---

# IoCs in Threat Intelligence

Threat Intelligence teams continuously share:

- Malicious IPs
- Domains
- URLs
- Hashes

SOC analysts use these IoCs to:

- Block threats
- Search SIEM logs
- Hunt compromised devices

---

# IoAs in Threat Hunting

Threat hunters search for attacker behavior rather than known malware.

Example hunts include:

- Office applications launching PowerShell
- Suspicious LSASS access
- Encoded PowerShell commands
- Credential dumping attempts

---

# Real-World Example

Alert:

```
WINWORD.exe
        ↓
powershell.exe
        ↓
powershell downloads payload
        ↓
LSASS accessed
        ↓
Dropbox upload
```

### IoAs

- Word spawning PowerShell
- LSASS access
- PowerShell download

### IoCs

- Dropbox domain
- File hash
- Malicious IP
- Downloaded executable

---

# Why This Matters

Modern SOC analysts don't only investigate **what has already happened**.

They also identify **what is happening right now**.

The best analysts combine:

- IoCs
- IoAs
- Threat Intelligence
- MITRE ATT&CK
- Detection Engineering

to stop attacks before significant damage occurs.

---

# Key Takeaways

- IoCs are evidence that a compromise has occurred.
- IoAs are behaviors that indicate an attack is in progress.
- IoCs are signature-based and reactive.
- IoAs are behavior-based and proactive.
- Modern SOCs rely heavily on IoAs because attacker behaviors are harder to change than malware signatures.
- Effective investigations combine both IoCs and IoAs to detect, investigate, and contain cyber threats.
