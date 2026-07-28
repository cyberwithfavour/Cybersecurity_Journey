# Day 61 – Cyber Kill Chain vs MITRE ATT&CK

## Objective

Understand the Cyber Kill Chain, compare it with the MITRE ATT&CK Framework, and learn how SOC analysts use both frameworks during threat detection, incident response, and threat hunting.

---

# What is the Cyber Kill Chain?

The **Cyber Kill Chain** is a cybersecurity framework developed by **Lockheed Martin** in 2011.

It describes the stages an attacker follows to successfully compromise a target.

The goal of the framework is simple:

> Break the attack at any stage before the attacker achieves their objective.

Unlike MITRE ATT&CK, which focuses on attacker behavior, the Cyber Kill Chain focuses on the **overall attack lifecycle**.

---

# Why Was It Created?

Before the Cyber Kill Chain, organizations mostly reacted after attacks had already succeeded.

Lockheed Martin introduced the framework to help defenders:

- Understand attacker progression
- Detect attacks earlier
- Interrupt attacks before damage occurs
- Improve defensive strategies

---

# The Seven Stages of the Cyber Kill Chain

## 1. Reconnaissance

The attacker gathers information about the target.

Examples:

- OSINT
- Google Dorking
- Social media research
- DNS enumeration
- Employee profiling

Goal:

Identify weaknesses before launching an attack.

---

## 2. Weaponization

The attacker prepares the attack.

Examples:

- Creating malware
- Embedding malware into documents
- Creating malicious links
- Building phishing emails

Goal:

Prepare a payload that will compromise the victim.

---

## 3. Delivery

The attacker sends the payload to the victim.

Examples:

- Phishing email
- Malicious USB
- Compromised website
- Drive-by download

Goal:

Get the payload to the target.

---

## 4. Exploitation

The victim interacts with the payload.

Examples:

- Opening a malicious attachment
- Clicking a phishing link
- Exploiting a software vulnerability

Goal:

Execute malicious code on the victim's system.

---

## 5. Installation

Malware installs itself on the compromised system.

Examples:

- Installing ransomware
- Creating scheduled tasks
- Installing persistence mechanisms

Goal:

Maintain access to the compromised device.

---

## 6. Command and Control (C2)

The compromised device communicates with the attacker's infrastructure.

Examples:

- Reverse shells
- Beaconing
- HTTPS connections
- DNS tunneling

Goal:

Allow the attacker to remotely control the compromised system.

---

## 7. Actions on Objectives

The attacker completes their mission.

Examples:

- Data theft
- Ransomware deployment
- Privilege escalation
- Destroying systems
- Financial fraud

Goal:

Achieve the intended objective.

---

# Visual Overview

```
Reconnaissance
        ↓
Weaponization
        ↓
Delivery
        ↓
Exploitation
        ↓
Installation
        ↓
Command & Control
        ↓
Actions on Objectives
```

---

# MITRE ATT&CK vs Cyber Kill Chain

| Cyber Kill Chain | MITRE ATT&CK |
|------------------|--------------|
| 7 attack stages | Hundreds of attacker behaviors |
| Linear model | Non-linear model |
| Focuses on attack lifecycle | Focuses on attacker techniques |
| Simpler to understand | More detailed and comprehensive |
| Strategic view | Tactical and operational view |

---

# Key Differences

## Cyber Kill Chain

Answers:

> **Where is the attacker in the attack lifecycle?**

---

## MITRE ATT&CK

Answers:

> **Exactly what technique is the attacker using?**

---

# Example

An attacker sends a phishing email.

## Cyber Kill Chain

Stage:

Delivery

---

## MITRE ATT&CK

Technique:

Phishing

T1566

---

The Kill Chain tells you **where**.

MITRE tells you **how**.

---

# Advantages of the Cyber Kill Chain

- Easy to understand
- Excellent for explaining attacks
- Useful for incident response planning
- Helps identify where attacks can be interrupted

---

# Limitations of the Cyber Kill Chain

- Assumes attacks always follow a straight path
- Does not describe modern attacker techniques in detail
- Less useful for threat hunting
- Does not cover insider threats well

---

# Advantages of MITRE ATT&CK

- Based on real-world attacker behavior
- Extremely detailed
- Continuously updated
- Excellent for detection engineering
- Supports threat hunting
- Used by SOCs worldwide

---

# Limitations of MITRE ATT&CK

- More complex
- Larger learning curve
- Requires practice to use effectively

---

# When SOC Analysts Use Each Framework

### Cyber Kill Chain

- Understanding the overall attack progression
- Incident response planning
- Executive reporting
- Security awareness training

---

### MITRE ATT&CK

- Threat hunting
- SIEM detection rules
- Alert investigation
- Threat intelligence
- Detection engineering
- Purple team exercises

---

# Example Attack

Attack:

- Phishing email delivered
- User opens attachment
- PowerShell executes
- Malware installed
- Remote command established
- Files stolen

### Cyber Kill Chain

- Delivery
- Exploitation
- Installation
- Command & Control
- Actions on Objectives

### MITRE ATT&CK

- T1566 – Phishing
- T1204 – User Execution
- T1059.001 – PowerShell
- T1105 – Ingress Tool Transfer
- T1071 – Application Layer Protocol
- T1567 – Exfiltration to Cloud Storage

---

# Which Framework is Better?

Neither framework replaces the other.

The Cyber Kill Chain provides a **high-level view** of an attack.

MITRE ATT&CK provides a **detailed breakdown** of attacker behavior.

Modern SOC teams often use **both frameworks together**.

---

# Why This Matters

During investigations, a SOC analyst should be able to answer two questions:

1. **Where is the attacker in the attack lifecycle?** (Cyber Kill Chain)

2. **What exact techniques are being used?** (MITRE ATT&CK)

Understanding both frameworks allows analysts to detect attacks faster, respond more effectively, and improve organizational defenses.

---

# Key Takeaways

- The Cyber Kill Chain was developed by Lockheed Martin.
- It consists of seven stages that describe the lifecycle of a cyberattack.
- MITRE ATT&CK focuses on attacker tactics and techniques.
- The Cyber Kill Chain provides the big picture, while MITRE ATT&CK provides detailed attacker behaviors.
- Both frameworks complement each other and are widely used in modern Security Operations Centers.
