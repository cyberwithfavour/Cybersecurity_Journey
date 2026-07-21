# Day 54 – Tasks

## Task 1

Define the following terms in your own words.

- Domain Name System (DNS)
- DNS Resolver
- DNS Cache
- DNS Spoofing
- DNS Tunneling
- DNS Hijacking
- DNS Amplification

---

## Task 2

Complete the table below.

| DNS Record | Purpose | Example |
|------------|---------|---------|
| A | | |
| AAAA | | |
| CNAME | | |
| MX | | |
| TXT | | |

---

## Task 3

Answer the following questions.

### 1.

Why is DNS often referred to as the "phonebook of the Internet"?

---

### 2.

Why do attackers commonly abuse DNS during cyber attacks?

---

### 3.

Why is DNS traffic difficult to block completely?

---

### 4.

Which DNS attack is commonly used for:

- Data Exfiltration?
- DDoS Attacks?
- Redirecting users to fake websites?

---

## Task 4

Think Like a SOC Analyst

While reviewing DNS logs, you observe the following:

```
Host: HR-PC-04

09:12 login.microsoftonline.com

09:13 office.com

09:14 kjh73hfj3j2kjsdfh.biz

09:14 kjh73hfj3j2kjsdfh.biz

09:15 kjh73hfj3j2kjsdfh.biz

09:16 kjh73hfj3j2kjsdfh.biz
```

Answer the following:

- What looks suspicious?
- What type of attack could this indicate?
- What additional logs would you investigate?
- What would be your next action as a SOC analyst?

---

## Task 5

Research the following public DNS providers.

For each provider, write:

- Primary Use
- Advantages
- Organization

Providers:

- Google Public DNS
- Cloudflare DNS
- Quad9
- OpenDNS

---

## Practical Exercise

Use the command below on your own computer (Windows Command Prompt or PowerShell):

```
nslookup google.com
```

Observe the output and identify:

- DNS Server
- IP Address returned
- Record Type (if shown)

If you cannot perform the exercise, explain what information **nslookup** provides and why it is useful during troubleshooting and security investigations.
