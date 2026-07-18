# Day 51 – Tasks

## Theory Questions

### Question 1

What is a firewall, and what is its primary purpose?

---

### Question 2

Differentiate between a hardware firewall and a software firewall.

---

### Question 3

Explain the difference between a stateless firewall and a stateful firewall.

---

### Question 4

What information does a packet-filtering firewall examine before making a decision?

---

### Question 5

What is a Next-Generation Firewall (NGFW), and how does it differ from a traditional firewall?

---

### Question 6

What is an Access Control List (ACL)?

---

### Question 7

Explain the difference between inbound traffic and outbound traffic.

---

### Question 8

Why is network segmentation important in cybersecurity?

---

# Practical Task

## SOC Investigation #006

### Scenario

The organization's firewall generated the following alert:

> **"Outbound connection blocked. Host 192.168.15.35 attempted to establish an HTTPS (TCP 443) connection to IP address 185.231.54.20, a known malicious IP listed in the organization's threat intelligence feed."**

The firewall automatically blocked the connection and forwarded the alert to the SIEM.

As the Tier 1 SOC Analyst, your responsibilities are to:

- Review the firewall alert.
- Identify the internal source host.
- Identify the external destination IP.
- Determine why the firewall blocked the connection.
- Assess the severity of the incident.
- Decide whether the incident should be escalated.
- Document your findings.

---

## Deliverables

Create a new folder in your **SOC-Labs** repository:

```text
Investigation_006_Blocked_Firewall_Alert
```

Inside the folder, create:

- README.md
- Alert_Investigation_Report.md
- Evidence.md
- Timeline.md
- Lessons_Learned.md

---

## Objective

Practice investigating a firewall alert involving a blocked outbound connection to a known malicious IP address and document the investigation using the standard SOC workflow.
