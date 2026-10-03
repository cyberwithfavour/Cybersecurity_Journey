# Day 67 — Threat Hunting: Suspicious Scheduled Tasks

## Focus
Threat Hunting / Persistence / SOC Analysis

## Objective

Learn how attackers can abuse Windows Scheduled Tasks to maintain persistence or execute commands, and how a SOC analyst can investigate suspicious scheduled-task activity.

---

# 1. What Are Scheduled Tasks?

Windows Scheduled Tasks allow Windows or applications to automatically perform an action at a specific time or when a specific event occurs.

Legitimate uses include:

- System maintenance
- Software updates
- Backups
- Security scans
- Automated administrative tasks
- Application maintenance

Scheduled Tasks are therefore not inherently malicious.

The SOC analyst's job is to determine whether a task is legitimate or suspicious.

---

# 2. Why Scheduled Tasks Matter to a SOC Analyst

Attackers may create or modify scheduled tasks to:

- Maintain persistence
- Execute commands automatically
- Run malicious programs
- Run PowerShell scripts
- Execute programs at specific times
- Re-establish activity after a reboot

This makes Scheduled Tasks an important persistence technique to monitor.

---

# 3. Threat Hunting Hypothesis

> An attacker may create or modify a Windows Scheduled Task to maintain persistence or execute commands on a compromised endpoint.

A hypothesis is not a conclusion.

The investigation must determine whether the task is:

- Benign
- Suspicious
- Potentially malicious
- Confirmed malicious

---

# 4. Legitimate vs Suspicious Scheduled Tasks

## Legitimate Example

```text
Task Name:
WindowsUpdateCheck

Action:
C:\Program Files\Windows Update\update.exe

Creator:
SYSTEM

Purpose:
Authorized system maintenance
