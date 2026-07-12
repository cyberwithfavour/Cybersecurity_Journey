# Day 24 – Single Sign-On (SSO), Federation & Identity Management

## Objective

Understand Single Sign-On (SSO), Federated Identity Management, Identity Providers (IdP), Service Providers (SP), and the protocols used for modern authentication.

---

# What is Single Sign-On (SSO)?

Single Sign-On (SSO) is an authentication method that allows users to log in once and access multiple applications without signing in again.

Example:

An employee logs into Microsoft 365 once and can access:
- Outlook
- Teams
- OneDrive
- SharePoint

without entering their password multiple times.

---

# Benefits of SSO

- Fewer passwords to remember.
- Better user experience.
- Increased productivity.
- Reduced password fatigue.
- Lower helpdesk costs from password resets.

---

# Disadvantages of SSO

- If one account is compromised, multiple systems may be affected.
- Requires strong security controls such as MFA.

---

# What is Identity Federation?

Identity Federation is a trust relationship between different organizations or systems that allows users to use one identity across multiple domains.

Example:

A university student logs into a learning platform using their university account instead of creating a new account.

---

# Federated Identity Management (FIM)

Federated Identity Management allows identities to be shared securely between trusted organizations.

Benefits:
- Users maintain one identity.
- Organizations avoid creating duplicate accounts.
- Simplifies collaboration.

Example:

A company uses Google Workspace accounts to access Salesforce.

---

# Identity Provider (IdP)

The Identity Provider is responsible for:

- Verifying user identities.
- Authenticating users.
- Providing authentication information to other services.

Examples:
- Microsoft Entra ID (formerly Azure AD)
- Google Identity
- Okta
- Auth0

Think of the IdP as the "security guard" that confirms who you are.

---

# Service Provider (SP)

A Service Provider is the application or service the user wants to access.

Examples:
- Salesforce
- Dropbox
- Slack
- Zoom

The Service Provider trusts the Identity Provider to authenticate users.

---

# Authentication Flow

User

↓

Identity Provider (IdP)

↓

Authentication

↓

Service Provider (SP)

↓

Access Granted

---

# Security Assertion Markup Language (SAML)

SAML is an XML-based standard used for exchanging authentication information between an Identity Provider and a Service Provider.

Commonly used in:
- Enterprise environments
- Corporate web applications

Benefits:
- Enables SSO.
- Secure authentication.

---

# OAuth 2.0

OAuth is an authorization framework.

Important:

OAuth **does not authenticate users.**

Instead, it allows applications to access resources on behalf of a user without sharing passwords.

Example:

"Continue with Google"

An application requests permission to access your Google profile.

---

# OpenID Connect (OIDC)

OpenID Connect builds on OAuth 2.0 by adding authentication.

Purpose:
- Authenticate users.
- Verify identity.

Used by:
- Google Sign-In
- Microsoft Sign-In
- Facebook Login

---

# SAML vs OAuth vs OpenID Connect

SAML
- Authentication
- Enterprise applications

OAuth
- Authorization
- API access

OpenID Connect
- Authentication
- Built on OAuth 2.0

---

# Why This Matters in Cybersecurity

Organizations use SSO and federation to:
- Improve user experience.
- Strengthen security.
- Simplify identity management.
- Reduce password reuse.
- Support cloud environments.

---

# Key Takeaways

- SSO allows one login for multiple applications.
- Identity Federation enables trusted identity sharing.
- IdPs authenticate users.
- SPs provide services.
- SAML supports enterprise SSO.
- OAuth provides authorization.
- OpenID Connect adds authentication to OAuth.
