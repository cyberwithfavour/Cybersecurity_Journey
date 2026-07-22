# Day 58 – Reflection

## What I Learned

Today's lesson taught me that protecting a network isn't just about installing firewalls or antivirus software. It's also about deciding **who can communicate with whom** inside the network.

I learned that **network segmentation** divides a large network into smaller, secure sections, making it harder for attackers to move freely if they compromise one system.

I also understood how **VLANs** make this possible without requiring separate physical networks. Different departments can share the same switch while remaining logically isolated from one another.

Another important concept was **microsegmentation**. Unlike traditional segmentation, which separates departments, microsegmentation protects individual servers and workloads by allowing only specific communication between systems.

Finally, I learned about **lateral movement**, where attackers move from one compromised device to other systems within the network. Proper segmentation is one of the best ways to slow down or completely stop this type of attack.

---

## Key Takeaway

Good network segmentation doesn't stop attacks from happening—it limits how far attackers can go after gaining initial access.

---

## Personal Reflection

Today's lesson helped me understand why enterprise networks are designed with so many layers and restrictions. What used to look like unnecessary complexity is actually intentional security.

As a future SOC analyst, knowing how a network is segmented will help me identify attacker movement, determine which systems are at risk, and recommend effective containment strategies during an investigation.
