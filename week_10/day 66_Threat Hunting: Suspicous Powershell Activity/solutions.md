# Day 66 — Solutions

## Task 1 — Hunting Hypothesis

### Answer

> An attacker may use PowerShell to execute commands on an endpoint after gaining unauthorized access.

### Why?

The hypothesis gives the investigation a specific behavior to search for instead of searching randomly.

---

# Task 2 — Identify Suspicious Indicators

Given:

```text
User: Sarah
Hostname: HR-LAPTOP-04
Process: powershell.exe
Parent Process: winword.exe
Command: powershell.exe -EncodedCommand [encoded content]
Time: 02:14 AM
Network Connection: External IP
```

### Indicators requiring investigation

1. PowerShell execution
2. Microsoft Word launching PowerShell
3. Encoded PowerShell command
4. Activity occurring at 02:14 AM
5. External network connection

### Does this prove compromise?

**No.**

These are suspicious characteristics that require investigation.

The analyst still needs additional evidence and context.

---

# Task 3 — Investigate the User

### Answers

1. The account associated with the activity is **Sarah**.
2. The department provided is **HR**.
3. Whether Sarah normally requires PowerShell must be verified.
4. Whether Sarah was expected to be working at 02:14 AM must also be verified.

### Important

Do not assume that an HR employee cannot legitimately use PowerShell.

The analyst should verify the user's normal responsibilities and activity.

---

# Task 4 — Process Chain

### Answer

```text
winword.exe
     ↓
powershell.exe
     ↓
Encoded Command
```

### Why is the parent process important?

It helps the analyst understand what caused PowerShell to start.

A Microsoft Word document launching PowerShell may require investigation because malicious documents can sometimes be used to trigger command execution.

However, the process relationship alone does not prove malicious activity.

### Additional evidence

The analyst should investigate:

* The document involved
* Document source
* User activity
* PowerShell command
* File creation
* Network activity
* Related endpoint events

---

# Task 5 — Encoded Command

### Answers

### 1. What does `-EncodedCommand` indicate?

It indicates that the PowerShell command has been encoded rather than presented directly in readable form.

### 2. What should the analyst do?

The analyst should safely decode and analyze the command according to the organization's investigation procedures.

### 3. Questions to answer

* What does the command execute?
* Does it download a file?
* Does it create a file?
* Does it connect to an external system?
* Does it collect information?
* Does it modify the system?
* Does it establish persistence?

---

# Task 6 — Network Connection

### Information to collect

The analyst should investigate:

* Destination IP
* Destination domain
* Port
* Protocol
* Timestamp
* DNS activity
* Proxy activity
* Firewall logs
* Threat-intelligence information
* Whether other endpoints contacted the same destination

### What would increase suspicion?

For example:

```text
Encoded PowerShell
        +
Unexpected parent process
        +
Unusual user activity
        +
External connection
        +
Known malicious destination
```

The combination provides stronger evidence than any single indicator.

### Does an external connection prove malicious activity?

**No.**

Legitimate applications and administrative activities also communicate with external systems.

---

# Task 7 — Evidence Correlation

A suitable investigation chain is:

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
```

The purpose is to correlate multiple pieces of evidence.

---

# Task 8 — Classification

### Classification

**Suspicious — Pending Further Investigation**

### Reason

The activity contains multiple characteristics that warrant investigation:

* PowerShell execution
* Word launching PowerShell
* Encoded command
* Unusual execution time
* External network connection

However, there is not enough evidence in the scenario to definitively establish malicious activity.

---

# Task 9 — MITRE ATT&CK

### Technique

**Command and Scripting Interpreter: PowerShell**

### Technique ID

**T1059.001**

### Reason

PowerShell was used to execute a command on the endpoint.

---

# Task 10 — SOC Analyst Response

If additional investigation confirms unauthorized activity, the SOC should:

1. Preserve relevant evidence.
2. Identify the affected endpoint.
3. Investigate the PowerShell command.
4. Identify the account involved.
5. Review authentication activity.
6. Investigate the external destination.
7. Search other endpoints for related indicators.
8. Escalate according to the incident-response process.
9. Contain the affected endpoint or account when appropriate.
10. Document the investigation.

---

# Task 11 — Analyst Conclusion

### Example

**Initial Finding:**

Suspicious PowerShell activity was identified on an endpoint.

**Evidence:**

The activity involved PowerShell being launched by Microsoft Word, an encoded command, unusual execution time, and an external network connection.

**Assessment:**

The activity is suspicious and requires further investigation. The available evidence does not independently confirm compromise.

**Next Step:**

Analyze the encoded command, investigate the external destination, review related endpoint and authentication logs, and search for the same indicators across the environment.

---

# Task 12 — GitHub Practice

Recommended structure:

```text
Day-66-Threat-Hunting-Suspicious-PowerShell/
│
├── notes.md
├── tasks.md
└── solutions.md
```

This separates your:

**Learning → Practice → Answer/Review**

and makes the repository useful for revision later.

---

# Final Challenge — Solution

## 1. Initial Observation

The alert shows PowerShell execution on a finance workstation.

The activity has several characteristics requiring investigation:

* Outlook launched PowerShell.
* The PowerShell command was encoded.
* The activity occurred at 01:47 AM.
* The endpoint communicated with an external IP.

---

## 2. Hunting Hypothesis

> An attacker may be abusing PowerShell to execute commands on the endpoint after gaining unauthorized access.

---

## 3. Evidence to Collect

The analyst should collect:

* User information
* Endpoint information
* PowerShell command
* Parent-child process information
* PowerShell logs
* Windows Event Logs
* EDR telemetry
* Authentication logs
* DNS logs
* Firewall/proxy logs
* Destination IP information
* Related file activity

---

## 4. Investigation

### User

Determine whether the user was expected to be active at 01:47 AM.

### Parent Process

Investigate why Outlook launched PowerShell.

### Command

Decode and analyze the PowerShell command according to approved investigation procedures.

### Network

Investigate the external IP and determine whether the connection was legitimate or suspicious.

### Correlation

Search for related activity before and after the PowerShell execution.

---

## 5. Findings

### Initial Finding

The activity is **suspicious and requires further investigation**.

The available evidence includes several correlated indicators, but the scenario does not provide enough information to definitively confirm malicious activity.

---

## 6. Risk Assessment

**Medium — Pending Further Investigation**

The severity may increase if further evidence confirms:

* Unauthorized access
* Malicious command execution
* Malicious network communication
* Credential theft
* Persistence
* Lateral movement

---

## 7. MITRE ATT&CK

**T1059.001 — Command and Scripting Interpreter: PowerShell**

---

## 8. Recommended Response

The SOC should:

1. Preserve evidence.
2. Investigate the PowerShell command.
3. Investigate the affected account.
4. Investigate the endpoint.
5. Investigate the external IP.
6. Search for related indicators across the environment.
7. Escalate if malicious activity is confirmed.
8. Contain the endpoint or account when appropriate.

---

## 9. Analyst Conclusion

> The alert represents suspicious PowerShell activity involving an unusual parent process, encoded command, unusual execution time, and external network communication. These indicators warrant further investigation, but the available evidence is insufficient to independently confirm compromise. Additional endpoint, authentication, and network evidence should be analyzed before determining the final classification.

---

# Final Lesson

The most important lesson from Day 66 is:

> **An alert is a starting point, not a conclusion.**

A SOC Analyst should move from:

```text
ALERT
 ↓
HYPOTHESIS
 ↓
EVIDENCE
 ↓
CORRELATION
 ↓
ANALYSIS
 ↓
CONCLUSION
```

rather than:

```text
ALERT
 ↓
"IT IS MALICIOUS"
```

**Day 66 Status:** Completed — Simulated Investigation

**Focus:** Threat Hunting / SOC Analysis

**MITRE ATT&CK:** T1059.001 — PowerShell
