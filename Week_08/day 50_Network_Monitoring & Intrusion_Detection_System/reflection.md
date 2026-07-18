# Day 50 – Reflection

## What I Learned

Today I learned how organizations monitor their networks to detect suspicious activity before it becomes a major security incident.

I now understand that an Intrusion Detection System (IDS) monitors traffic and generates alerts, while an Intrusion Prevention System (IPS) can automatically block malicious traffic.

I also learned the difference between Network-based IDS (NIDS) and Host-based IDS (HIDS), as well as the strengths and weaknesses of signature-based and anomaly-based detection.

One important takeaway is that not every alert means an attack has occurred. Security analysts must investigate alerts carefully because they could be false positives, while false negatives are even more dangerous because malicious activity goes undetected.

Finally, I learned how IDS and IPS fit into a SOC workflow by sending alerts to a SIEM, where analysts investigate and respond to potential threats.

---

## Challenges

At first, I confused IDS and IPS because they perform similar functions.

I also needed to understand when to use Network-based IDS versus Host-based IDS.

---

## How I Solved Them

I compared them using simple examples:

- IDS = Security Camera (Detects and alerts)
- IPS = Security Guard (Detects and blocks)

This made it much easier to remember their roles.

I also related today's lesson to my previous studies on SIEM and network traffic analysis, which helped me see how all the concepts connect in a real SOC environment.

---

## Key Takeaway

Effective cybersecurity is not just about detecting attacks but understanding which alerts require investigation and which can be safely dismissed. Knowing how IDS, IPS, and SIEM work together is essential for every SOC analyst.

---

## Skills Gained Today

- Network Monitoring
- IDS vs IPS
- NIDS vs HIDS
- Signature-Based Detection
- Anomaly-Based Detection
- False Positives & False Negatives
- SOC Alert Workflow
