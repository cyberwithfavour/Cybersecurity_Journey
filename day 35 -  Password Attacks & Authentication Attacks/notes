# Day 35 – Password Attacks & Authentication Attacks

## Objective

Understand common password attacks, authentication attacks, and the security controls used to defend against them.

---

# Why Attack Passwords?

Passwords are often the first line of defense protecting systems and accounts.

Attackers target passwords because gaining valid credentials allows them to access systems without exploiting software vulnerabilities.

Compromised credentials are one of the leading causes of data breaches.

---

# Common Password Attacks

## 1. Brute Force Attack

A Brute Force Attack attempts every possible password combination until the correct one is found.

Characteristics:

- Very slow
- Can eventually succeed
- More effective against weak passwords

Example:

Trying:

123456

123457

123458

...

until access is gained.

Prevention:

- Strong passwords
- Account lockout
- MFA

---

## 2. Dictionary Attack

A Dictionary Attack uses a list of common passwords instead of every possible combination.

Examples:

password

welcome

qwerty

admin123

This attack is faster than brute force.

Prevention:

- Complex passwords
- Password policies
- MFA

---

## 3. Password Spraying

Instead of trying many passwords on one account, attackers try one common password against many accounts.

Example:

Password:

Welcome123

Accounts:

user1

user2

user3

user4

This avoids triggering account lockouts.

Prevention:

- MFA
- Strong password policy
- Detect repeated login attempts

---

## 4. Credential Stuffing

Credential Stuffing uses usernames and passwords stolen from previous data breaches.

Attackers assume users reuse passwords.

Example:

A password leaked from one website is used to access:

- Gmail
- Netflix
- Microsoft
- Banking apps

Prevention:

- Unique passwords
- Password manager
- MFA

---

## 5. Rainbow Table Attack

A Rainbow Table contains precomputed password hashes.

Attackers compare stolen password hashes against the table.

Prevention:

- Salting passwords
- Strong hashing algorithms
- MFA

---

## 6. Keylogger

A Keylogger records every key pressed on a keyboard.

Goals:

- Capture passwords
- Capture banking details
- Capture confidential information

Keyloggers may be:

- Software
- Hardware

Prevention:

- Anti-malware software
- MFA
- Regular system scans

---

## 7. Shoulder Surfing

Attackers physically watch users type passwords.

Examples:

- ATM
- Coffee shop
- Office

Prevention:

- Privacy screens
- Awareness
- Shield the keyboard

---

## 8. Default Password Attack

Attackers attempt manufacturer default usernames and passwords.

Examples:

admin/admin

root/root

Prevention:

- Change default credentials immediately.

---

# Authentication Attacks

Authentication attacks target the login process itself.

Examples include:

- Password attacks
- Session hijacking
- Pass-the-Hash
- Replay attacks

---

## Pass-the-Hash Attack

Instead of stealing the password itself, attackers steal the password hash.

The hash is reused to authenticate without knowing the original password.

Commonly targets Windows environments.

Prevention:

- Least Privilege
- Credential Guard
- Patch systems

---

## Replay Attack

An attacker captures valid authentication data and retransmits it later.

Goal:

Pretend to be the legitimate user.

Prevention:

- Nonces
- Session tokens
- Encryption
- Time stamps

---

# Multi-Factor Authentication (MFA)

MFA requires two or more authentication factors.

Something you know

- Password
- PIN

Something you have

- Phone
- Security key

Something you are

- Fingerprint
- Face recognition

Benefits:

Even if attackers steal a password, access is still blocked.

---

# Password Best Practices

Use:

- Long passwords (12–16+ characters)
- Passphrases
- Password managers
- Unique passwords
- MFA

Avoid:

- Reusing passwords
- Personal information
- Simple patterns

---

# Why Password Security Matters

Weak passwords remain one of the easiest ways for attackers to gain unauthorized access.

Strong authentication significantly reduces cyber risk.

---

# Key Takeaways

- Brute Force tries every possible password.
- Dictionary Attacks use common passwords.
- Password Spraying targets many users with one password.
- Credential Stuffing relies on reused passwords.
- Rainbow Tables attack password hashes.
- Keyloggers capture keystrokes.
- MFA provides additional protection.
