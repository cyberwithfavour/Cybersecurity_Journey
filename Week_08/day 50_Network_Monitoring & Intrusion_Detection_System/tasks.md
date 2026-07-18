# Day 50 – Tasks

## Theory Questions

### Question 1
What is network monitoring?

---

### Question 2
What is the primary difference between an IDS and an IPS?

---

### Question 3
Differentiate between Network-based IDS (NIDS) and Host-based IDS (HIDS).

---

### Question 4
What is signature-based detection?

---

### Question 5
What is anomaly-based detection?

---

### Question 6
Explain the difference between a false positive and a false negative.

---

### Question 7
Name three open-source IDS/IPS solutions.

---

### Question 8
Briefly explain how an IDS works with a SIEM in a SOC environment.

---

# Practical Task

## SOC Investigation #005

### Scenario

The organization's **Network Intrusion Detection System (NIDS)** generated the following alert:

> **"Multiple TCP SYN packets detected from IP address 192.168.10.25 targeting ports 21, 22, 23, 80, 135, 139, 445, and 3389 on an internal server within 30 seconds."**

The IDS classified the activity as a **Potential Port Scan**.

As the Tier 1 SOC Analyst, your responsibilities are to:

- Review the IDS alert.
- Identify the source IP address.
- Identify the targeted ports.
- Determine what type of attack is suspected.
- Assess the severity of the alert.
- Decide whether the incident should be escalated.
- Document the investigation.

---

## Deliverables

Create a new folder in your **SOC-Labs** repository:

```text
Investigation_005_Potential_Port_Scan
```

Inside the folder, create:

- README.md
- Alert_Investigation_Report.md
- Evidence.md
- Timeline.md
- Lessons_Learned.md

---

## Objective

Practice investigating an IDS-generated alert and documenting your findings using the standard SOC investigation workflow.
