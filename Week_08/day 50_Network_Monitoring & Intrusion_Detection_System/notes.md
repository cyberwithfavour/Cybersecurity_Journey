# Day 50 – Network Monitoring & Intrusion Detection Systems (IDS/IPS)

## What is Network Monitoring?

Network monitoring is the continuous observation of network traffic, devices, and services to detect abnormal or malicious activity.

The goal is to maintain the availability, performance, and security of a network.

Security teams monitor networks to:

- Detect cyber attacks
- Identify suspicious behavior
- Detect malware communication
- Monitor network performance
- Respond quickly to incidents

---

## What is an IDS?

An Intrusion Detection System (IDS) is a security solution that monitors network or host activity for suspicious behavior and generates alerts when potential threats are detected.

An IDS does NOT block attacks.

Its primary function is detection.

Think of an IDS as a security camera.

It watches everything and notifies security personnel when something suspicious happens.

---

## What is an IPS?

An Intrusion Prevention System (IPS) performs the same monitoring functions as an IDS but can automatically stop or block malicious traffic.

Think of an IPS as a security guard.

It not only detects suspicious activity but also takes action.

---

## IDS vs IPS

IDS
- Detects attacks
- Generates alerts
- Does not block traffic
- Passive

IPS
- Detects attacks
- Blocks malicious traffic
- Active protection

---

## Types of IDS

### Network-based IDS (NIDS)

Monitors traffic moving across the network.

Examples:
- Snort
- Suricata
- Zeek

---

### Host-based IDS (HIDS)

Installed on individual computers or servers.

Monitors:

- System files
- Processes
- Registry
- Logins
- File integrity

Examples:

- OSSEC
- Wazuh

---

## Detection Methods

### Signature-Based Detection

Detects known attacks by comparing activity against a database of attack signatures.

Advantages

- Fast
- Accurate for known threats

Disadvantages

- Cannot detect unknown attacks

---

### Anomaly-Based Detection

Builds a baseline of normal behavior and alerts when activity deviates from that baseline.

Advantages

- Detects unknown attacks

Disadvantages

- Higher false positive rate

---

## False Positive

A legitimate activity incorrectly identified as malicious.

Example:

A security scan performed by the IT team triggers an IDS alert.

---

## False Negative

A malicious activity that is not detected.

Example:

A new malware variant bypasses signature detection.

---

## IDS/IPS in a SOC

Typical workflow:

1. IDS detects suspicious activity.
2. Alert is forwarded to the SIEM.
3. SIEM correlates multiple events.
4. Tier 1 analyst validates the alert.
5. Investigation begins.
6. Incident is escalated if necessary.

---

## Common IDS/IPS Solutions

Open Source

- Snort
- Suricata
- Zeek
- Wazuh

Commercial

- Cisco Secure IPS
- Palo Alto Threat Prevention
- Fortinet IPS
- Trend Micro Deep Security

---

## Key Terms

- Network Monitoring
- IDS
- IPS
- NIDS
- HIDS
- Signature Detection
- Anomaly Detection
- False Positive
- False Negative
- Threat Detection
- Alert
- Prevention
