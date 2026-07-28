# Day 61 – Practical Investigation

## Scenario

You are a **Tier 1 SOC Analyst** working in the Security Operations Center.

At **08:45 AM**, your SIEM generates several alerts involving a Finance employee.

The alerts show the following sequence:

- The attacker researches the company's employees on LinkedIn.
- A phishing email containing an Excel attachment is sent.
- The employee opens the attachment.
- A malicious macro launches PowerShell.
- Malware is installed on the workstation.
- The infected workstation begins communicating with an external Command & Control (C2) server.
- The attacker steals confidential financial records.

Your SOC manager wants you to analyze the incident using **both the Cyber Kill Chain and the MITRE ATT&CK Framework**.

---

# Practical Tasks

## Step 1 – Build the Attack Timeline

Create a timeline of the attack from the first attacker action to the final objective.

Document every stage in chronological order.

---

## Step 2 – Map the Cyber Kill Chain

Using the seven stages of the Cyber Kill Chain, identify where each attacker action belongs.

Create a table showing:

- Attacker Action
- Kill Chain Stage
- Explanation

---

## Step 3 – Map MITRE ATT&CK

Using the MITRE ATT&CK Framework, identify:

- ATT&CK Tactic
- ATT&CK Technique
- ATT&CK ID

for each attacker action.

---

## Step 4 – Compare Both Frameworks

Write a comparison showing:

- What information the Cyber Kill Chain gives you.
- What additional information MITRE ATT&CK provides.
- Which framework gives more detail during an investigation.
- Why SOC analysts often use both together.

---

## Step 5 – Identify Detection Opportunities

Assume your organization wants to detect the attack earlier.

Identify at least **six places** where the SOC could have detected or interrupted the attack.

Examples include:

- Email Security Gateway
- Microsoft Defender
- PowerShell Logging
- EDR Alerts
- Firewall Logs
- Network IDS/IPS

Explain what would be detected at each stage.

---

## Step 6 – Containment Plan

The attacker is still connected to the compromised workstation.

Document the first actions you would take as the responding SOC analyst.

Your response should include:

- Endpoint actions
- User account actions
- Network actions
- Evidence preservation
- Escalation procedures

---

# GitHub Deliverable

Create the following folder structure:

```text
Week09/
└── Day61_KillChain_vs_MITRE/
```

Include these files:

- `attack_timeline.md`
- `kill_chain_mapping.md`
- `mitre_mapping.md`
- `framework_comparison.md`
- `incident_report.md`

---

# Objective

By completing this investigation, you should be able to:

- Analyze a real-world cyberattack using the Cyber Kill Chain.
- Analyze the same attack using MITRE ATT&CK.
- Understand the strengths of both frameworks.
- Document an investigation using industry-standard methodologies.
