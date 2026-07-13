# Day 20 – Network Monitoring & Troubleshooting

## Objective

Understand how network administrators and cybersecurity professionals monitor, troubleshoot, and diagnose network problems using common tools and commands.

---

# What is Network Monitoring?

Network monitoring is the continuous observation of a network to ensure it operates efficiently, securely, and without interruption.

Monitoring helps identify:
- Network failures
- Performance issues
- Security incidents
- Unauthorized devices
- Unusual traffic

Benefits:
- Detects problems early.
- Improves network performance.
- Reduces downtime.
- Enhances security.

---

# Network Troubleshooting

Network troubleshooting is the process of identifying, diagnosing, and resolving network problems.

Common issues include:
- No Internet connection
- Slow network speed
- Packet loss
- DNS failures
- IP address conflicts
- Faulty cables
- Firewall misconfigurations

---

# Common Network Troubleshooting Tools

## Ping

The `ping` command tests connectivity between two devices.

It works by sending ICMP Echo Requests and waiting for Echo Replies.

Example:

ping google.com

If replies are received, the destination is reachable.

If no replies are received, there may be a network problem.

---

## Traceroute (traceroute)

Traceroute shows the path packets take from your device to another device.

It identifies every router (hop) along the journey.

Example:

traceroute google.com

Useful for:
- Finding delays
- Locating routing problems

---

## ip

The `ip` command displays network configuration information.

Examples:

ip a

Displays:
- IP address
- MAC address
- Network interfaces

hostname -I

Displays the system's IP address.

---

## nslookup

The `nslookup` command checks DNS resolution.

Example:

nslookup google.com

It shows:
- DNS server used
- IP address returned

Useful for diagnosing DNS issues.

---

## netstat

The `netstat` command displays active network connections and listening ports.

Example:

netstat -tuln

Useful for:
- Viewing open ports
- Detecting suspicious services

---

## ss

The `ss` command is the modern replacement for netstat.

Example:

ss -tuln

Shows:
- TCP connections
- UDP connections
- Listening services

---

# Packet Capture

Packet capture involves recording network traffic for analysis.

Common Tool:
Wireshark

Uses:
- Troubleshooting
- Incident response
- Malware analysis
- Protocol analysis

---

# Log Monitoring

Logs record activities performed by systems, users, and applications.

Examples:
- Login attempts
- Firewall events
- VPN connections
- System errors

Logs help security teams:
- Detect attacks
- Investigate incidents
- Meet compliance requirements

---

# Indicators of Network Problems

Common symptoms include:
- Slow Internet
- Frequent disconnections
- High latency
- Packet loss
- Failed DNS lookups
- Services becoming unavailable

---

# Basic Troubleshooting Process

1. Identify the problem.
2. Gather information.
3. Form a possible cause.
4. Test the solution.
5. Verify the issue is resolved.
6. Document the findings.

---

# Why Network Monitoring Matters

Cybersecurity professionals monitor networks to:
- Detect intrusions.
- Identify malware communication.
- Investigate suspicious traffic.
- Ensure systems remain available.

Without monitoring, attacks may go unnoticed.

---

# Key Takeaways

- Monitoring helps detect problems before they become major incidents.
- Ping tests connectivity.
- Traceroute shows packet paths.
- nslookup verifies DNS.
- ip displays network configuration.
- netstat and ss display active connections and open ports.
- Wireshark captures network traffic.
- Logs are essential during incident investigations.
