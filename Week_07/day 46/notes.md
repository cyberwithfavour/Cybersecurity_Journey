# Day 46 Notes – Introduction to Security Operations Center (SOC)

## What is a Security Operations Center (SOC)?

A Security Operations Center (SOC) is a centralized team responsible for continuously monitoring, detecting, investigating, and responding to cybersecurity threats within an organization.

The SOC serves as the organization's first line of defense against cyberattacks.

---

# Goals of a SOC

- Monitor security events
- Detect suspicious activity
- Investigate security alerts
- Respond to incidents
- Minimize business impact
- Improve organizational security

---

# SOC Analyst Tiers

## Tier 1 Analyst (Alert Analyst)

Responsibilities:

- Monitor SIEM dashboards
- Review alerts
- Validate alerts
- Gather evidence
- Escalate confirmed incidents
- Document investigations

Tier 1 analysts are the first responders within a SOC.

---

## Tier 2 Analyst (Incident Responder)

Responsibilities:

- Investigate complex alerts
- Perform malware analysis
- Contain security incidents
- Coordinate incident response
- Support Tier 1 analysts

---

## Tier 3 Analyst (Threat Hunter)

Responsibilities:

- Threat hunting
- Detection engineering
- Threat intelligence
- SIEM rule development
- Advanced investigations

---

# Event vs Alert vs Incident

## Event

Any activity occurring on a system.

Example:
A user logs into a workstation.

---

## Alert

A notification generated when suspicious activity matches predefined security rules.

Example:
15 failed login attempts.

---

## Incident

A confirmed security event that requires action.

Example:
An attacker successfully compromises a user account.

---

# Alert Investigation Workflow

1. Receive Alert
2. Validate Alert
3. Gather Evidence
4. Analyze Findings
5. Determine Severity
6. Escalate if necessary
7. Document Investigation

---

# Severity Levels

Low

- Minimal impact

Medium

- Requires investigation

High

- Immediate response required

Critical

- Significant business impact

---

# Key Concepts

Security Information and Event Management (SIEM)

A SIEM collects, analyzes, and correlates security logs to help analysts detect threats.

Common SIEM solutions include:

- Microsoft Sentinel
- Splunk
- IBM QRadar
- Elastic SIEM

---

# Key Takeaways

- Not every alert is an incident.
- Evidence determines whether an alert is malicious.
- Documentation is an essential SOC responsibility.
- Tier 1 analysts form the first line of cyber defense.
