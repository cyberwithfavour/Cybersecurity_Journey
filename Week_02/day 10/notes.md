# Day 10 – Network Topologies & Network Communication

## Objective

Learn how devices are physically and logically connected in a network and understand how data travels between them.

---

## What is a Network Topology?

A network topology is the physical or logical arrangement of devices in a network.

It describes how computers, switches, routers, and other devices are connected.

Choosing the right topology affects:
- Performance
- Reliability
- Scalability
- Cost
- Fault tolerance

---

## Types of Network Topologies

### 1. Bus Topology

All devices share a single communication cable called the backbone.

Advantages:
- Easy to install
- Low cost
- Uses less cable

Disadvantages:
- If the backbone fails, the whole network stops working.
- Performance decreases as more devices are added.

---

### 2. Star Topology

Every device connects to a central switch or hub.

Advantages:
- Easy to troubleshoot.
- One device failing does not affect others.
- Most common topology in modern organizations.

Disadvantages:
- If the central switch fails, the entire network goes down.

---

### 3. Ring Topology

Each device connects to two neighboring devices, forming a circle.

Advantages:
- Data flows in an organized manner.
- No data collisions.

Disadvantages:
- Failure of one device can disrupt communication.

---

### 4. Mesh Topology

Every device connects directly to every other device.

Advantages:
- High reliability.
- Excellent redundancy.
- Multiple communication paths.

Disadvantages:
- Expensive.
- Complex to install.

---

### 5. Hybrid Topology

A combination of two or more topologies.

Example:
A company may combine Star and Bus topologies.

Advantages:
- Flexible.
- Scalable.
- Common in large organizations.

---

## Data Communication

For devices to communicate, three things are required:

- Sender
- Communication Medium
- Receiver

Example:

Laptop → Router → Internet → Server

---

## Communication Media

### Wired Media

Uses physical cables.

Examples:
- Ethernet cable
- Fiber optic cable

Advantages:
- Faster
- More reliable
- Better security

---

### Wireless Media

Uses radio signals.

Examples:
- Wi-Fi
- Bluetooth

Advantages:
- Mobility
- Convenience

---

## Bandwidth

Bandwidth is the maximum amount of data that can be transmitted over a network in a given period.

Measured in:
- Mbps
- Gbps

Higher bandwidth means more data can travel at once.

---

## Latency

Latency is the delay before data reaches its destination.

Measured in milliseconds (ms).

Lower latency means faster communication.

Example:
Online gaming requires low latency.

---

## Throughput

Throughput is the actual amount of data successfully transferred across a network.

Unlike bandwidth, throughput reflects real-world performance.

---

## Why This Matters in Cybersecurity

Understanding network topologies helps security professionals:
- Identify single points of failure.
- Design secure networks.
- Improve redundancy.
- Troubleshoot connectivity issues.

Knowledge of bandwidth, latency, and throughput also helps detect abnormal network behavior during attacks.

---

## Key Takeaways

- Network topology describes how devices are connected.
- Star topology is the most commonly used today.
- Mesh topology offers the highest redundancy.
- Bandwidth measures capacity.
- Latency measures delay.
- Throughput measures actual performance.
