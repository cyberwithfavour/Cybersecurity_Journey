# Day 47 Notes – SIEM Fundamentals & Security Monitoring

## What is a SIEM?

A **Security Information and Event Management (SIEM)** system is a security solution that collects, stores, analyzes, and correlates logs from different devices and applications across an organization's environment.

Its main purpose is to help security teams detect suspicious activities, investigate incidents, and respond to threats more efficiently.

Think of a SIEM as the **central hub** where security data from different sources comes together for analysis.

---

# Why Do Organizations Use SIEM?

Organizations use SIEM solutions to:

- Centralize security logs
- Monitor networks and systems in real time
- Detect suspicious activities
- Investigate security incidents
- Meet compliance requirements
- Improve incident response

Without a SIEM, analysts would have to manually check logs from every device, making it difficult to detect attacks quickly.

---

# SIEM Workflow

A SIEM follows a structured process:

## 1. Log Collection

The SIEM gathers logs from different devices and applications.

Examples include:

- Windows computers
- Linux servers
- Firewalls
- Antivirus software
- Active Directory
- Cloud services
- Web servers

---

## 2. Log Aggregation

Logs from multiple sources are collected and stored in one central location.

This makes investigation much easier because analysts no longer need to check each device individually.

---

## 3. Log Normalization

Different devices generate logs in different formats.

A SIEM converts these logs into a standardized format so they can be analyzed consistently.

---

## 4. Correlation

The SIEM compares logs from different systems to identify suspicious patterns.

Example:

- Multiple failed logins
- Successful login
- Login from another country

Individually these events may seem harmless, but together they may indicate a brute-force attack.

---

## 5. Alert Generation

When suspicious patterns match predefined rules, the SIEM generates an alert for the SOC analyst.

Example:

> "20 failed login attempts followed by a successful login."

---

## 6. Investigation

The SOC analyst reviews the alert by:

- Validating the alert
- Gathering evidence
- Assessing severity
- Escalating if necessary
- Documenting findings

---

# Common Log Sources

A SIEM collects logs from many different systems.

Examples include:

### Windows Event Logs
Contain login events, account changes, application logs, and system events.

### Linux Logs
Record authentication attempts, services, and system activities.

### Firewalls
Show allowed and blocked network traffic.

### IDS/IPS
Generate alerts for suspicious network behavior.

### Antivirus & EDR
Detect malware, ransomware, and endpoint threats.

### Active Directory
Records authentication events, account creation, and privilege changes.

### Cloud Platforms
Azure, AWS, and Microsoft 365 generate security and audit logs.

---

# Security Monitoring

Security monitoring is the continuous observation of systems and networks to detect threats before they become incidents.

A SOC analyst continuously monitors:

- Authentication attempts
- User activity
- Network traffic
- System changes
- Security alerts

---

# Microsoft Sentinel

Microsoft Sentinel is Microsoft's cloud-native SIEM and SOAR solution.

Key features:

- Cloud-based
- Collects logs from multiple sources
- Uses AI for threat detection
- Supports automated incident response
- Integrates with Microsoft Defender and Azure

---

# Splunk

Splunk is one of the most widely used SIEM platforms.

It helps analysts:

- Search logs
- Build dashboards
- Investigate incidents
- Create alerts
- Generate security reports

---

# SIEM vs SOAR

| SIEM | SOAR |
|------|------|
| Detects and analyzes threats | Automates security responses |
| Generates alerts | Executes response actions |
| Helps analysts investigate | Helps analysts respond faster |

---

# Key Terms

**Log:** A record of system activity.

**Event:** Any recorded activity on a system.

**Alert:** A notification generated when suspicious activity is detected.

**Correlation:** Combining multiple events to identify potential threats.

**Dashboard:** A visual interface showing security data and alerts.

**Rule:** A condition that tells the SIEM when to generate an alert.

---

# Key Takeaways

- SIEM centralizes security logs.
- SIEM helps detect suspicious activities.
- Correlation is one of the most powerful SIEM features.
- Logs are the foundation of every SOC investigation.
- SIEM allows analysts to investigate threats more efficiently.
