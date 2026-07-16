# Practical Tasks – Day 49

## Theory Tasks

### Task 1

What is network traffic, and why is it important for cybersecurity?

---

### Task 2

What is a packet?

List five pieces of information a packet can contain.

---

### Task 3

Explain the purpose of packet analysis.

---

### Task 4

What is Wireshark, and why is it commonly used by SOC analysts?

---

### Task 5

Differentiate between the following protocols:

- TCP
- UDP
- HTTP
- HTTPS
- DNS

---

### Task 6

Explain the TCP Three-Way Handshake.

---

### Task 7

Why is DNS important?

How can attackers abuse DNS?

---

### Task 8

List at least five indicators of suspicious network activity.

---

## Hands-on Investigation

### Scenario

A SIEM generated the following alert:

> **"One workstation generated more than 500 DNS requests to an unknown domain within 10 minutes."**

---

### Investigation Objectives

As a Tier 1 SOC Analyst:

1. Validate the alert.

2. Determine whether the DNS activity is normal or suspicious.

3. Identify what evidence should be collected.

4. Assess the severity.

5. Recommend immediate containment actions.

6. Decide whether the incident should be escalated.

---

## Portfolio Task

Complete this investigation in your **SOC-Labs** repository.

Create a new folder:

```text
Investigation_004_Suspicious_DNS_Traffic
```

Include:

- README.md
- Alert_Investigation_Report.md
- Evidence.md
- Timeline.md
- Lessons_Learned.md

---

## Stretch Task (Optional)

If you have Wireshark installed:

- Capture network traffic.
- Identify DNS packets.
- Identify HTTP or HTTPS packets.
- Record the protocols observed.
- Save screenshots for your portfolio.
