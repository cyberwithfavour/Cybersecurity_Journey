# Day 50 – Solutions

## Theory Questions

### Question 1
**What is network monitoring?**

Network monitoring is the continuous observation of network traffic, devices, and services to detect abnormal, suspicious, or malicious activity while ensuring the network remains secure and operational.

---

### Question 2
**What is the primary difference between an IDS and an IPS?**

- **IDS (Intrusion Detection System):** Detects suspicious activity and generates alerts but does not block traffic.
- **IPS (Intrusion Prevention System):** Detects suspicious activity and can automatically block or prevent malicious traffic.

---

### Question 3
**Differentiate between NIDS and HIDS.**

**NIDS (Network-based Intrusion Detection System)**
- Monitors network traffic.
- Detects attacks across the network.
- Installed at strategic points within the network.

**HIDS (Host-based Intrusion Detection System)**
- Installed on individual computers or servers.
- Monitors system files, processes, registry, and local events.
- Detects attacks targeting a specific host.

---

### Question 4
**What is signature-based detection?**

Signature-based detection compares network activity against a database of known attack signatures to identify known threats.

Advantages:
- Fast
- Accurate for known attacks

Disadvantages:
- Cannot detect new or unknown threats.

---

### Question 5
**What is anomaly-based detection?**

Anomaly-based detection establishes a baseline of normal network behavior and generates alerts whenever unusual activity deviates from that baseline.

Advantages:
- Detects unknown attacks.

Disadvantages:
- May produce more false positives.

---

### Question 6
**Explain the difference between a false positive and a false negative.**

**False Positive**
A legitimate activity is incorrectly identified as malicious.

Example:
An internal vulnerability scan triggers an IDS alert.

**False Negative**
Malicious activity occurs but is not detected.

Example:
A new malware variant bypasses detection.

---

### Question 7
**Name three open-source IDS/IPS solutions.**

- Snort
- Suricata
- Zeek

(Other acceptable answers include Wazuh and OSSEC.)

---

### Question 8
**Briefly explain how an IDS works with a SIEM in a SOC environment.**

The IDS monitors network or host activity and generates alerts when suspicious behavior is detected. These alerts are forwarded to the SIEM, where they are correlated with logs from other sources. Tier 1 SOC analysts review the alerts, validate them, collect evidence, determine severity, and escalate incidents when necessary.

---

# Practical Task – Expected Investigation

## Alert Type

Potential Port Scan

---

## Source IP

192.168.10.25

---

## Target Ports

- 21 (FTP)
- 22 (SSH)
- 23 (Telnet)
- 80 (HTTP)
- 135 (RPC)
- 139 (NetBIOS)
- 445 (SMB)
- 3389 (RDP)

---

## Suspicious Activity

A single host attempted to connect to multiple ports on the same server within a short period.

This behavior is commonly associated with **port scanning**, where an attacker attempts to discover open services before launching an attack.

---

## Severity

**Medium**

Reason:

No evidence of successful exploitation was observed, but reconnaissance activity is often the first phase of an attack.

---

## Recommended Actions

- Validate the IDS alert.
- Review firewall and network logs.
- Determine whether the scan originated from an authorized vulnerability scanner.
- Check whether additional hosts were targeted.
- Continue monitoring the source IP.
- Escalate to Tier 2 if the activity appears malicious or continues.

---

## Investigation Outcome

The activity was identified as a **suspected reconnaissance (port scanning) attempt**.

Additional investigation is required to determine whether the activity is authorized or malicious.
