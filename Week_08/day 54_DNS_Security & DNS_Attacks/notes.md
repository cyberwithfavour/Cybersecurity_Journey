# Day 54 – Notes

## What is DNS?

The **Domain Name System (DNS)** is a service that translates human-readable domain names into IP addresses.

Instead of remembering an IP address like **142.250.190.78**, users simply type a domain name such as **www.google.com**.

DNS acts as the **Internet's phonebook**, allowing devices to locate websites and services efficiently.

---

## Why is DNS Important?

Without DNS:

- Users would have to remember IP addresses.
- Websites would be difficult to access.
- Many Internet services would not function properly.

Almost every network communication begins with a DNS query.

---

## How DNS Works

When a user enters a website address into a browser:

1. The device sends a DNS query.
2. The DNS resolver searches for the corresponding IP address.
3. If the answer is not cached, the resolver queries other DNS servers.
4. The correct IP address is returned.
5. The browser connects to the destination server.

This entire process usually takes only a few milliseconds.

---

## Common DNS Record Types

### A Record

Maps a domain name to an IPv4 address.

Example:

```
google.com → 142.250.190.78
```

---

### AAAA Record

Maps a domain name to an IPv6 address.

---

### CNAME Record

Creates an alias for another domain.

Example:

```
www.company.com → company.com
```

---

### MX Record

Specifies the mail server responsible for receiving emails.

---

### TXT Record

Stores text information used for domain verification and email security technologies such as SPF, DKIM, and DMARC.

---

## DNS Caching

DNS servers temporarily store previously resolved domain names.

Benefits include:

- Faster browsing
- Reduced DNS traffic
- Improved performance

---

## Common DNS Attacks

### DNS Spoofing (Cache Poisoning)

An attacker inserts false DNS records into a DNS cache, causing users to be redirected to malicious websites.

---

### DNS Amplification Attack

A Distributed Denial-of-Service (DDoS) attack that exploits DNS servers to overwhelm a target with large amounts of traffic.

---

### DNS Tunneling

Attackers hide malicious communications inside DNS queries and responses.

DNS tunneling is commonly used for:

- Data exfiltration
- Command-and-Control (C2) communication
- Bypassing firewalls

---

### DNS Hijacking

An attacker changes DNS settings so users are redirected to malicious websites without their knowledge.

---

## Indicators of Suspicious DNS Activity

SOC analysts look for:

- Excessive DNS requests
- Long or random-looking domain names
- Frequent requests to unknown domains
- High volumes of TXT record queries
- DNS traffic outside business hours
- Connections to known malicious domains

---

## DNS Logging in a SOC Environment

DNS logs help analysts answer questions such as:

- Which domains were queried?
- Which device made the request?
- When did the query occur?
- Was the domain malicious?
- Was data potentially exfiltrated?

DNS logs are one of the most valuable data sources during threat hunting and incident investigations.

---

## Why DNS Matters to a SOC Analyst

Attackers often rely on DNS because organizations usually allow DNS traffic through firewalls.

Monitoring DNS activity helps analysts detect:

- Malware infections
- Phishing campaigns
- Command-and-Control communication
- Data exfiltration
- Suspicious network behavior

DNS analysis is a fundamental skill for every SOC analyst because nearly every cyberattack leaves traces in DNS logs.
