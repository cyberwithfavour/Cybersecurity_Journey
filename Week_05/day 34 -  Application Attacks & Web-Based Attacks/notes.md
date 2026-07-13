# Day 34 – Application Attacks & Web-Based Attacks

## Objective

Understand common web application attacks, how attackers exploit them, and the security controls used to prevent them.

---

# What are Application Attacks?

Application attacks target weaknesses in software or web applications to gain unauthorized access, steal data, or disrupt services.

Attackers often exploit:

- Poor coding practices
- Misconfigurations
- Lack of input validation
- Outdated software

---

# Common Web Application Attacks

## 1. SQL Injection (SQLi)

SQL Injection occurs when an attacker inserts malicious SQL commands into an application's input field.

Goal:

- Read database contents
- Modify records
- Delete data
- Bypass authentication

Example:

A login page accepts user input without validating it.

Instead of entering:

Username: John

An attacker enters:

' OR '1'='1

This may allow unauthorized access.

Prevention:

- Parameterized queries
- Prepared statements
- Input validation
- Least privilege database accounts

---

## 2. Cross-Site Scripting (XSS)

Cross-Site Scripting allows attackers to inject malicious JavaScript into a web page viewed by other users.

Goals:

- Steal session cookies
- Redirect users
- Capture keystrokes
- Deface websites

Types:

Stored XSS
- Malicious script is saved on the server.

Reflected XSS
- Script is reflected back immediately in the response.

DOM-Based XSS
- Attack occurs through client-side JavaScript.

Prevention:

- Input validation
- Output encoding
- Content Security Policy (CSP)

---

## 3. Cross-Site Request Forgery (CSRF)

CSRF tricks an authenticated user into performing unwanted actions without their knowledge.

Example:

A logged-in bank user visits a malicious website.

The website secretly submits a money transfer request using the user's existing session.

Prevention:

- CSRF tokens
- MFA
- Re-authentication for sensitive actions

---

## 4. Command Injection

Occurs when attackers execute operating system commands through an application.

Example:

Instead of entering a filename, an attacker enters:

file.txt && whoami

If successful, the server executes both commands.

Prevention:

- Validate user input
- Avoid system command execution
- Use allowlists

---

## 5. Directory Traversal (Path Traversal)

Allows attackers to access files outside the intended directory.

Example:

../../etc/passwd

Goal:

Access sensitive system files.

Prevention:

- Validate file paths
- Restrict file permissions
- Use allowlists

---

## 6. Buffer Overflow

Occurs when more data is written into memory than it can hold.

Effects:

- Application crash
- Code execution
- System compromise

Prevention:

- Secure coding
- Memory protection
- Input validation

---

## 7. XML External Entity (XXE)

Occurs when XML processors accept malicious external entities.

Attackers may:

- Read local files
- Access internal systems
- Cause denial of service

Prevention:

- Disable external entities
- Update XML parsers

---

## Input Validation

Applications should never trust user input.

Good validation includes:

- Length checks
- Type checks
- Character restrictions

Always validate data before processing it.

---

## Output Encoding

Output Encoding converts dangerous characters into safe formats before displaying them.

Helps prevent:

- Cross-Site Scripting (XSS)

---

## Secure Coding

Developers should:

- Validate all inputs.
- Sanitize outputs.
- Use parameterized queries.
- Handle errors securely.
- Update third-party libraries.

---

# Why Application Security Matters

Many data breaches occur because web applications contain vulnerabilities.

Secure coding and regular testing reduce these risks.

---

# Key Takeaways

- SQL Injection targets databases.
- XSS injects malicious JavaScript.
- CSRF tricks authenticated users into performing actions.
- Command Injection executes operating system commands.
- Directory Traversal accesses unauthorized files.
- Buffer Overflow exploits memory.
- Input validation and secure coding prevent many application attacks.
