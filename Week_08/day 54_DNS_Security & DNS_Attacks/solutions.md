# Day 54 – Solutions

## Task 1

### Domain Name System (DNS)

DNS is a service that translates human-readable domain names into IP addresses so devices can communicate over a network.

---

### DNS Resolver

A DNS resolver receives DNS queries from clients and finds the correct IP address by communicating with DNS servers.

---

### DNS Cache

A temporary storage location that saves previously resolved domain names to improve performance and reduce DNS traffic.

---

### DNS Spoofing

An attack where false DNS information is inserted into a DNS cache, causing users to be redirected to malicious websites.

---

### DNS Tunneling

A technique that hides malicious communication inside DNS traffic to bypass security controls and exfiltrate data.

---

### DNS Hijacking

An attack where DNS settings are modified so users are redirected to attacker-controlled websites.

---

### DNS Amplification

A DDoS attack that exploits open DNS servers to generate a large volume of traffic toward a victim.

---

## Task 2

| DNS Record | Purpose | Example |
|------------|---------|---------|
| A | Maps a hostname to an IPv4 address | google.com → 142.250.190.78 |
| AAAA | Maps a hostname to an IPv6 address | example.com → 2606:2800:220:1:248:1893:25c8:1946 |
| CNAME | Creates an alias for another domain | www.company.com → company.com |
| MX | Specifies the mail server for a domain | mail.company.com |
| TXT | Stores text information for verification and email security | SPF, DKIM, DMARC |

---

## Task 3

### 1. Why is DNS often referred to as the "phonebook of the Internet"?

Because it converts easy-to-remember domain names into IP addresses that computers use to communicate.

---

### 2. Why do attackers commonly abuse DNS during cyber attacks?

Because DNS traffic is almost always allowed through firewalls, making it an effective channel for hiding malicious communication.

---

### 3. Why is DNS traffic difficult to block completely?

Because nearly every application and website depends on DNS for name resolution. Blocking DNS would prevent users from accessing Internet resources.

---

### 4. Which DNS attack is commonly used for:

**Data Exfiltration?**

- DNS Tunneling

**DDoS Attacks?**

- DNS Amplification

**Redirecting users to fake websites?**

- DNS Spoofing (Cache Poisoning) or DNS Hijacking

---

## Task 4

### What looks suspicious?

The repeated queries to the unusual domain:

```
kjh73hfj3j2kjsdfh.biz
```

The domain name appears random and is repeatedly queried within a short period.

---

### What type of attack could this indicate?

Possible:

- DNS Tunneling
- Malware Command-and-Control (C2)
- Malware beaconing

---

### What additional logs would you investigate?

- Firewall logs
- Proxy logs
- Endpoint Detection and Response (EDR) logs
- Windows Event Logs
- DNS server logs
- Network traffic (PCAP)

---

### What would be your next action as a SOC analyst?

- Investigate the suspicious domain.
- Determine whether it is malicious using threat intelligence.
- Review the endpoint for malware.
- Isolate the host if compromise is suspected.
- Escalate the incident if malicious activity is confirmed.

---

## Task 5

### Google Public DNS

**Primary Use**

Public DNS resolution.

**Advantages**

- Fast
- Reliable
- Highly available

**Organization**

Google

---

### Cloudflare DNS

**Primary Use**

Public DNS with privacy focus.

**Advantages**

- Very fast
- Privacy-focused
- DNSSEC support

**Organization**

Cloudflare

---

### Quad9

**Primary Use**

Security-focused DNS service.

**Advantages**

- Blocks known malicious domains
- Uses threat intelligence feeds

**Organization**

Quad9 Foundation

---

### OpenDNS

**Primary Use**

Public DNS and content filtering.

**Advantages**

- Malware protection
- Web filtering
- Security reporting

**Organization**

Cisco

---

## Practical Exercise

### Command

```
nslookup google.com
```

### Example Output

```
Server: 8.8.8.8

Address: 8.8.8.8

Non-authoritative answer:

Name: google.com

Address: 142.250.190.78
```

### Information Provided

- DNS server being queried.
- IP address of the requested domain.
- Domain successfully resolved.
- Useful for verifying DNS functionality and troubleshooting name resolution issues.

### Why is nslookup useful?

SOC analysts and network administrators use **nslookup** to:

- Verify DNS resolution.
- Troubleshoot connectivity problems.
- Identify incorrect DNS records.
- Investigate suspicious domains during incident response.
