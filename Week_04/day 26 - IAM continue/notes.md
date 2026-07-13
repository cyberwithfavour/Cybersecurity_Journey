# Day 26 – Identity Lifecycle, Account Auditing & Access Reviews

## Objective

Understand how organizations manage user identities throughout their lifecycle, perform access reviews, and audit user accounts to maintain security.

---

# What is Identity Lifecycle Management (ILM)?

Identity Lifecycle Management (ILM) is the process of managing a user's digital identity from the moment they join an organization until they leave.

The identity lifecycle ensures users have the right access at the right time.

Stages include:
- Join
- Move
- Leave

---

# Join

When a new employee joins:

IT creates:
- User account
- Email
- Username
- Initial password
- Required permissions

Example:

A new SOC Analyst receives:
- Microsoft account
- VPN access
- SIEM access
- Email account

---

# Move

Employees often change departments or roles.

Example:

A Help Desk Technician becomes a Security Analyst.

IT should:

- Remove old permissions.
- Assign new permissions.

Never keep unnecessary permissions.

This prevents "Privilege Creep."

---

# Leave

When an employee leaves:

The organization should immediately:

- Disable the account.
- Remove VPN access.
- Disable email.
- Recover company devices.
- Remove administrator privileges.

Failure to do this creates serious security risks.

---

# What is Privilege Creep?

Privilege Creep occurs when users gradually accumulate permissions they no longer need.

Example:

Employee joins HR.

↓

Transfers to Finance.

↓

Transfers to IT.

If old permissions remain, the employee now has unnecessary access to multiple departments.

Risks:

- Insider threats
- Data breaches
- Unauthorized access

---

# Access Reviews

Access Reviews involve regularly checking user permissions.

Questions asked:

- Does this user still need this access?
- Has the employee changed roles?
- Should this account still exist?

Organizations perform reviews:
- Monthly
- Quarterly
- Annually

---

# Account Auditing

Account auditing involves reviewing user accounts to identify security issues.

Things to check:

- Inactive accounts
- Dormant accounts
- Disabled accounts
- Privileged accounts
- Shared accounts
- Failed login attempts

Benefits:

- Detects unnecessary access.
- Supports compliance.
- Improves security.

---

# User Activity Logs

Every action performed by users should be logged.

Examples:

- Login attempts
- Password changes
- File access
- Permission changes
- Administrator actions

Logs help investigators during security incidents.

---

# Recertification

Recertification means managers periodically confirm that users still require their assigned permissions.

Example:

Manager reviews employee permissions every six months.

If unnecessary permissions exist:

Remove them immediately.

---

# Offboarding

Offboarding is the secure removal of access when someone leaves an organization.

Checklist:

- Disable account.
- Reset passwords.
- Remove MFA devices.
- Recover laptops.
- Disable VPN.
- Archive email if necessary.

Good offboarding reduces insider threats.

---

# Why Identity Lifecycle Management Matters

Poor identity management may result in:

- Former employees accessing systems.
- Excessive permissions.
- Insider attacks.
- Compliance violations.

Strong lifecycle management keeps organizations secure.

---

# Key Takeaways

- Identity Lifecycle follows Join → Move → Leave.
- Privilege Creep occurs when users accumulate unnecessary permissions.
- Access Reviews verify users still need their permissions.
- Account Auditing identifies risky accounts.
- Recertification confirms permissions remain appropriate.
- Offboarding removes access immediately when users leave.
