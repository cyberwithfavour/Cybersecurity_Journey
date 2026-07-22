# Day 58 – Notes

# Network Segmentation

Network Segmentation is the practice of dividing a large network into smaller, isolated sections to improve security, performance, and management.

Instead of allowing every device to communicate with every other device, segmentation creates separate network areas with controlled communication between them.

For example, an organization may separate:

- Human Resources
- Finance
- IT Department
- Guest Wi-Fi
- Servers
- Security Cameras
- VoIP Phones

Each section becomes its own protected environment.

---

# Why Network Segmentation Matters

Without segmentation:

- Malware spreads quickly.
- Attackers move freely across the network.
- Sensitive data becomes easier to access.
- Network traffic becomes difficult to manage.

With segmentation:

- Attacks are contained.
- Sensitive systems remain protected.
- Network performance improves.
- Monitoring becomes easier.
- Access control becomes more effective.

---

# Benefits of Network Segmentation

A properly segmented network provides:

- Better Security
- Improved Performance
- Easier Troubleshooting
- Better Compliance
- Reduced Attack Surface
- Easier Monitoring

---

# VLAN (Virtual Local Area Network)

A VLAN is a logical method of dividing devices into separate networks, even when they are connected to the same physical switch.

Instead of buying multiple switches, administrators can create multiple virtual networks on a single switch.

Example:

Switch

- VLAN 10 → HR
- VLAN 20 → Finance
- VLAN 30 → IT
- VLAN 40 → Guest Network

Although everyone uses the same switch, each department operates in its own isolated network.

---

# Why Organizations Use VLANs

VLANs help organizations:

- Separate departments
- Improve security
- Reduce unnecessary network traffic
- Simplify administration
- Prevent unauthorized communication

---

# Inter-VLAN Communication

Devices in different VLANs cannot communicate directly.

A Layer 3 device (usually a router or Layer 3 switch) is required to allow communication between VLANs.

This allows administrators to control exactly which VLANs are allowed to communicate.

Example:

- HR can access Payroll Server.
- Guest Network cannot access Internal Servers.
- Finance can access Database Server.

---

# East-West Traffic

East-West traffic refers to communication between devices inside the same organization.

Examples:

- PC communicating with File Server.
- Workstation communicating with Database Server.
- Employee laptop accessing Internal Applications.

Attackers often use East-West traffic for lateral movement after gaining access to a network.

---

# North-South Traffic

North-South traffic refers to communication entering or leaving the organization's network.

Examples:

- User browsing the Internet.
- Customer accessing a company website.
- Employee downloading updates.

Firewalls primarily monitor North-South traffic.

---

# Microsegmentation

Microsegmentation takes network segmentation one step further.

Instead of protecting entire departments, security policies are applied to individual systems or workloads.

Example:

Inside the Finance VLAN:

- Payroll Server communicates only with Payroll Application.
- Database communicates only with Application Server.
- Employee PCs cannot directly access the database.

Even if an attacker compromises one device, movement is heavily restricted.

---

# Network Segmentation vs Microsegmentation

| Network Segmentation | Microsegmentation |
|----------------------|------------------|
| Separates departments or large network sections. | Separates individual systems and workloads. |
| Reduces large-scale attacks. | Prevents lateral movement between individual devices. |
| Uses VLANs, routers, and firewalls. | Uses software-defined security policies and host-based controls. |

---

# Lateral Movement

Lateral Movement occurs when an attacker moves from one compromised device to another inside the same network.

Example:

Internet

↓

Employee PC

↓

File Server

↓

Domain Controller

↓

Database Server

Good segmentation helps stop this movement before critical systems are reached.

---

# Segmentation in Enterprise Security

Modern organizations commonly separate:

- User Devices
- Servers
- Domain Controllers
- Database Servers
- Cloud Resources
- IoT Devices
- Guest Networks
- Management Networks

Each segment has its own security policies and access controls.

---

# Why This Matters to a SOC Analyst

SOC analysts investigate attacks across enterprise networks.

Understanding segmentation helps analysts:

- Determine how an attacker entered the network.
- Identify which systems are affected.
- Detect lateral movement.
- Recommend containment strategies.
- Reduce the impact of security incidents.

Many real-world investigations involve determining whether proper segmentation prevented an attacker from reaching critical systems.
