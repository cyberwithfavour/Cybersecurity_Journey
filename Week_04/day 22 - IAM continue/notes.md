# Day 22 – Authentication Factors & Authentication Methods

## Objective

Understand the different authentication factors, authentication methods, and how they strengthen security.

---

# What is Authentication?

Authentication is the process of verifying that a user, device, or system is who it claims to be.

It answers the question:

"Can you prove your identity?"

Authentication happens before authorization.

---

# Authentication Factors

Authentication factors are categories of evidence used to verify identity.

There are five major authentication factors.

---

# 1. Something You Know

Information only the user should know.

Examples:
- Password
- PIN
- Passphrase
- Security question

Advantages:
- Easy to implement.

Disadvantages:
- Can be guessed.
- Can be stolen through phishing.

---

# 2. Something You Have

A physical object owned by the user.

Examples:
- Smartphone
- Smart card
- Security token
- Hardware key (YubiKey)

Advantages:
- Difficult for attackers to duplicate.

---

# 3. Something You Are

Biometric authentication based on physical characteristics.

Examples:
- Fingerprint
- Face recognition
- Iris scan
- Retina scan
- Voice recognition

Advantages:
- Convenient.
- Difficult to copy.

Disadvantages:
- May require specialized hardware.

---

# 4. Somewhere You Are

Authentication based on location.

Examples:
- GPS location
- Corporate office network
- Country or region

Example:
A company allows logins only from Nigeria.

---

# 5. Something You Do

Behavioral authentication.

Examples:
- Typing pattern
- Signature
- Mouse movement
- Walking pattern

Used mainly in advanced security systems.

---

# Single-Factor Authentication (SFA)

Uses only one authentication factor.

Example:
Password only.

Advantages:
- Simple.

Disadvantages:
- Less secure.

---

# Multi-Factor Authentication (MFA)

Uses two or more different authentication factors.

Example:

Password
+
Fingerprint

or

Password
+
One-Time Password (OTP)

Benefits:
- Stronger security.
- Reduces account compromise.

---

# Two-Factor Authentication (2FA)

A specific type of MFA using exactly two authentication factors.

Example:

Password
+
SMS Code

or

Password
+
Authenticator App

---

# One-Time Password (OTP)

An OTP is a temporary password that expires after one use or a short period.

Examples:
- SMS verification code
- Email verification code
- Authenticator app code

Benefits:
- Protects against password reuse.

---

# Hardware Security Keys

A hardware security key is a physical authentication device.

Examples:
- YubiKey
- FIDO2 Security Keys

Benefits:
- Resistant to phishing.
- Strong authentication.

---

# Authenticator Apps

Applications that generate temporary authentication codes.

Examples:
- Google Authenticator
- Microsoft Authenticator
- Authy

Advantages:
- More secure than SMS.
- Works offline after setup.

---

# SMS Authentication

Authentication codes are sent by text message.

Advantages:
- Easy to use.

Disadvantages:
- Vulnerable to SIM swapping attacks.

---

# Why MFA Matters

Most data breaches involve compromised passwords.

Even if an attacker steals a password, MFA provides another layer of protection.

This significantly reduces the likelihood of unauthorized access.

---

# Key Takeaways

- Authentication verifies identity.
- Five authentication factors exist.
- Passwords belong to "Something You Know."
- Biometrics belong to "Something You Are."
- MFA combines two or more different factors.
- 2FA is a type of MFA using exactly two factors.
- Authenticator apps are generally more secure than SMS verification.
