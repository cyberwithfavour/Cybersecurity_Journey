# Day 46 – Solutions

## Theory Task 1

### Explain the purpose of a Security Operations Center (SOC).

A Security Operations Center (SOC) is a centralized team responsible for continuously monitoring, detecting, investigating, and responding to cybersecurity threats within an organization. The SOC works 24/7 to protect an organization's systems, networks, and data by identifying suspicious activities, minimizing security risks, and responding to incidents before they cause significant damage.

The primary goals of a SOC are to:
- Monitor security events across the organization.
- Detect and investigate potential threats.
- Respond to security incidents quickly.
- Reduce the impact of cyberattacks.
- Improve the organization's overall security posture.

---

## Theory Task 2

### Compare the responsibilities of Tier 1, Tier 2, and Tier 3 SOC Analysts.

| Tier | Responsibilities |
|------|------------------|
| **Tier 1 (Alert Analyst)** | Monitors security alerts, validates alerts, gathers evidence, documents findings, and escalates confirmed incidents. |
| **Tier 2 (Incident Responder)** | Performs deeper investigations, analyzes malware, contains incidents, identifies root causes, and supports Tier 1 analysts. |
| **Tier 3 (Threat Hunter)** | Conducts proactive threat hunting, develops detection rules, researches advanced threats, and improves SOC detection capabilities. |

---

## Theory Task 3

### Differentiate between an Event, Alert, and Incident.

**Event**
An event is any activity that occurs on a system or network. Events are not necessarily malicious.

*Example:* A user successfully logs into their workstation.

**Alert**
An alert is a notification generated when suspicious activity matches predefined security rules.

*Example:* Fifteen failed login attempts from the same IP address.

**Incident**
An incident is a confirmed security event that requires immediate investigation and response.

*Example:* An attacker successfully gains unauthorized access to a user account.

---

## Theory Task 4

### Describe the Security Alert Investigation Workflow.

A standard security alert investigation follows these steps:

1. Receive the alert.
2. Validate whether the alert is genuine.
3. Collect evidence such as logs, IP addresses, timestamps, and user activity.
4. Analyze the collected information.
5. Determine the severity of the event.
6. Escalate the case if necessary.
7. Document the investigation and findings.

---

## Theory Task 5

### Why is documentation important in a SOC?

Documentation is important because it:

- Maintains an audit trail of investigations.
- Helps other analysts understand previous actions.
- Supports compliance and legal requirements.
- Improves consistency during incident response.
- Provides lessons learned for future investigations.
- Enables better communication within the SOC team.

---

# Practical Investigation

## Scenario

A SIEM generated the following alert:

> **15 failed login attempts followed by one successful login from Germany.**

### Initial Assessment

The alert appears suspicious because multiple failed authentication attempts were immediately followed by a successful login from an unfamiliar geographic location. This could indicate a brute-force or credential stuffing attack.

### Evidence to Collect

- Username
- Source IP address
- Login timestamps
- Device information
- Geographic location
- Previous login history
- Authentication logs
- Windows Event Logs or Linux authentication logs
- VPN usage (if applicable)

### Severity

**High**

**Reason:**
- Multiple failed login attempts
- Successful authentication after repeated failures
- Login from an unusual country
- Possible account compromise

### Recommended Actions

- Escalate the alert to a Tier 2 analyst.
- Contact the user to verify the login.
- Lock or disable the account if compromise is suspected.
- Force a password reset.
- Block the suspicious IP address if confirmed malicious.
- Continue monitoring for additional suspicious activity.

### Conclusion

Based on the available information, this alert should be treated as a potential account compromise until proven otherwise. Further investigation is required before determining whether it is a true security incident.

---

# Portfolio Reference

A detailed investigation report for this scenario will be maintained in my **SOC-Labs** repository as:

**Investigation_001 – Suspicious Login Investigation**

This separates my learning notes from my practical cybersecurity portfolio while documenting the same investigation in a professional format.
