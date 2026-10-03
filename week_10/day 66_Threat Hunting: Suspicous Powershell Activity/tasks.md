# Day 66 — Tasks

## Topic

**Threat Hunting — Suspicious PowerShell Activity**

---

# Task 1 — Create a Hunting Hypothesis

Write a threat-hunting hypothesis for suspicious PowerShell activity.

Your hypothesis should answer:

> What suspicious behavior am I looking for?

---

# Task 2 — Identify Suspicious Indicators

From the following activity, identify the indicators that should make a SOC Analyst investigate further.

```text
User: Sarah
Hostname: HR-LAPTOP-04
Process: powershell.exe
Parent Process: winword.exe
Command: powershell.exe -EncodedCommand [encoded content]
Time: 02:14 AM
Network Connection: External IP
```

### Questions

1. Which indicators are suspicious?
2. Which indicators require additional context?
3. Does this information alone prove compromise?

---

# Task 3 — Investigate the User

Answer:

1. Who executed PowerShell?
2. What department does the user belong to?
3. Would this user's job normally require PowerShell?
4. Was the user expected to be working at the time?

---

# Task 4 — Investigate the Process Chain

Complete the process chain:

```text
__________
     ↓
powershell.exe
     ↓
Encoded Command
```

Then answer:

1. What is the parent process?
2. Why is the parent process important?
3. What additional evidence would you look for?

---

# Task 5 — Investigate the Command

The command contains:

```text
-EncodedCommand
```

Answer:

1. What does this indicate?
2. What should the SOC Analyst do next?
3. What questions should be answered before classifying the activity as malicious?

---

# Task 6 — Investigate the Network Connection

The PowerShell process communicated with an external IP address.

Answer:

1. What information would you collect about the IP?
2. What logs could help?
3. What would make the connection more suspicious?
4. Would an external connection alone prove malicious activity?

---

# Task 7 — Evidence Correlation

Complete the investigation chain:

```text
User
 ↓
__________
 ↓
__________
 ↓
__________
 ↓
Network Activity
 ↓
__________
```

Use the investigation fields from today's notes.

---

# Task 8 — Classification

Based on the information provided, classify the activity as:

* Benign
* Suspicious
* Potentially Malicious

Then explain **why**.

Your explanation should contain evidence rather than simply stating your classification.

---

# Task 9 — MITRE ATT&CK

Identify the relevant MITRE ATT&CK technique.

Write:

```text
Technique:
Technique ID:
Reason:
```

---

# Task 10 — SOC Analyst Response

Assume additional investigation confirms that the PowerShell activity was unauthorized.

List **at least 5 actions** the SOC should take.

---

# Task 11 — Analyst Conclusion

Write a short SOC Analyst conclusion using this structure:

```text
Initial Finding:
Evidence:
Assessment:
Next Step:
```

Do not simply say:

> "This is malware."

Explain your reasoning.

---

# Task 12 — GitHub Practice

Create a folder:

```text
Day-66-Threat-Hunting-Suspicious-PowerShell
```

Inside it, create:

```text
notes.md
tasks.md
solutions.md
```

Do not copy the solutions into your task answers before attempting the investigation.

---

# Final Challenge

Imagine you are working in a SOC.

You receive this alert:

```text
ALERT: Suspicious PowerShell Activity

User: David
Host: FINANCE-PC07
Parent Process: outlook.exe
Process: powershell.exe
Command: Encoded PowerShell command
Time: 01:47 AM
Network: Connection to an external IP
```

Write a complete investigation using:

```text
1. Initial Observation
2. Hunting Hypothesis
3. Evidence to Collect
4. Investigation
5. Findings
6. Risk Assessment
7. MITRE ATT&CK
8. Recommended Response
9. Analyst Conclusion
```

### Important

Do not assume that the alert automatically means the machine is compromised.

Investigate the evidence first.
