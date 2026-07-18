# Day 51 – Reflection

## What I Learned

Today I learned about firewalls and how they help protect networks by controlling the traffic entering and leaving an organization.

I learned that a firewall acts as the first line of defense by allowing legitimate traffic while blocking unauthorized or suspicious connections based on predefined security rules.

I also understood the differences between hardware and software firewalls, as well as packet filtering, stateless firewalls, stateful firewalls, and Next-Generation Firewalls (NGFWs).

Another important concept I learned is network segmentation. Separating different parts of a network helps reduce the impact of an attack because an attacker cannot easily move from one network to another.

Finally, I learned that firewall logs are valuable in a SOC because they are forwarded to the SIEM, where analysts investigate suspicious traffic and determine whether further action is needed.

---

## Challenges

At first, I found it difficult to distinguish between stateless and stateful firewalls because they both inspect network traffic.

I also wanted to better understand how ACLs and firewall rules work together to control access.

---

## How I Solved Them

I simplified the concepts by thinking of them this way:

- **Stateless Firewall** = Checks each packet independently without remembering previous traffic.
- **Stateful Firewall** = Remembers existing connections before deciding whether traffic should be allowed.

I also reviewed examples of inbound and outbound rules, which made ACLs easier to understand.

---

## Key Takeaway

A firewall is much more than a device that blocks traffic. It is a critical security control that helps organizations enforce security policies, monitor communication, and reduce the attack surface. Understanding how firewalls work is an essential skill for every SOC analyst.

---

## Skills Gained Today

- Firewall Fundamentals
- Hardware vs Software Firewalls
- Packet Filtering
- Stateful vs Stateless Firewalls
- Next-Generation Firewalls (NGFW)
- Access Control Lists (ACLs)
- Network Segmentation
- Firewall Logging
- SOC Network Defense
