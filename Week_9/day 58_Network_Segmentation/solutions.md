# Day 58 – Solutions

## Task 1

### Network Segmentation

The process of dividing a large network into smaller, isolated sections to improve security, performance, and access control.

---

### VLAN

A Virtual Local Area Network (VLAN) is a logical grouping of devices into separate networks, even when they are connected to the same physical switch.

---

### Microsegmentation

A security approach that isolates individual systems or workloads by applying specific communication rules between them.

---

### Lateral Movement

The technique attackers use to move from one compromised device to other systems within the same network.

---

### East-West Traffic

Traffic that moves between devices inside an organization's internal network.

---

### North-South Traffic

Traffic entering or leaving the organization's network, typically between internal systems and the Internet.

---

### Inter-VLAN Communication

Communication between devices in different VLANs through a Layer 3 device such as a router or Layer 3 switch.

---

### Layer 3 Switch

A network switch capable of performing routing functions, allowing communication between different VLANs.

---

## Task 2

| Concept | Purpose |
|---------|---------|
| Network Segmentation | Divides a network into smaller secure sections. |
| VLAN | Logically separates devices into different broadcast domains. |
| Microsegmentation | Restricts communication between individual systems and workloads. |
| East-West Traffic | Internal communication between devices within an organization. |
| North-South Traffic | Communication between the internal network and external networks. |
| Lateral Movement | Allows attackers to spread through a compromised network. |
| Inter-VLAN Communication | Enables controlled communication between separate VLANs. |
| Layer 3 Switch | Routes traffic between VLANs while enforcing security policies. |

---

## Task 3

### 1. Why is network segmentation important in enterprise security?

It limits attacker movement, protects sensitive systems, reduces the attack surface, improves monitoring, and strengthens access control.

---

### 2. What is the difference between a VLAN and microsegmentation?

A VLAN separates groups of devices or departments, while microsegmentation applies security policies to individual systems or workloads for more granular protection.

---

### 3. Why can't devices in different VLANs communicate directly?

Because each VLAN is a separate broadcast domain. Communication between VLANs requires a Layer 3 device to route traffic according to security policies.

---

### 4. Why do attackers often rely on lateral movement after compromising a device?

Their initial target may not contain valuable information, so they move through the network to reach critical systems such as file servers, databases, or domain controllers.

---

### 5. How does microsegmentation improve security compared to traditional network segmentation?

It provides much finer control by restricting communication between individual devices, making it significantly harder for attackers to move laterally.

---

## Task 4

### Five Security Weaknesses

- All departments share the same VLAN.
- Guest Wi-Fi is connected to the internal network.
- No separation between users and critical servers.
- No network segmentation to contain attacks.
- Domain Controller and Database Server are directly accessible from user devices.

---

### Systems at Risk

- Finance Department
- IT Department
- Database Server
- Domain Controller
- Other employee workstations

---

### How Proper Segmentation Helps

- Contains ransomware within the HR VLAN.
- Prevents direct access to critical servers.
- Restricts communication between departments.
- Reduces lateral movement.
- Limits the overall impact of the attack.

---

### Department That Should Never Share the Same Network as Guest Wi-Fi

Guest Wi-Fi should never share the same network as **any internal department**, especially Finance, HR, IT, or the Server Network.

---

### Security Recommendations

- Create separate VLANs for each department.
- Place Guest Wi-Fi on an isolated VLAN.
- Protect servers behind an internal firewall.
- Restrict Inter-VLAN communication using access control policies.
- Continuously monitor network traffic with IDS/IPS and SIEM solutions.

---

## Task 5

### Default VLAN

**Purpose**

The VLAN all switch ports belong to by default.

**Common Use**

Initial switch configuration.

---

### Data VLAN

**Purpose**

Carries normal user network traffic.

**Common Use**

Employee workstations and office devices.

---

### Voice VLAN

**Purpose**

Separates VoIP traffic from normal data traffic.

**Common Use**

IP phones and unified communications.

---

### Management VLAN

**Purpose**

Provides secure access for managing network devices.

**Common Use**

Switches, routers, firewalls, and network administrators.

---

### Native VLAN

**Purpose**

Carries untagged traffic across trunk links.

**Common Use**

Communication between network switches.

---

## Practical Exercise

### Example VLAN Assignment

| Department | VLAN |
|------------|-----:|
| Human Resources | VLAN 10 |
| Finance | VLAN 20 |
| IT | VLAN 30 |
| Sales | VLAN 40 |
| Guest Wi-Fi | VLAN 50 |
| Server Network | VLAN 60 |

---

### VLAN Communication

- HR ↔ Server Network (Allowed)
- Finance ↔ Server Network (Allowed)
- IT ↔ All VLANs (Controlled Administrative Access)
- Sales ↔ Server Network (Limited Access)
- Guest Wi-Fi ↔ Internet Only

---

### Firewall Placement

- Between the Internet and the internal network.
- Between the Server Network and user VLANs for additional protection.

---

### How This Design Reduces Lateral Movement

If an attacker compromises a device in one VLAN, they cannot freely access other departments or critical servers without passing through controlled security policies. This limits the spread of malware and helps contain security incidents quickly.
