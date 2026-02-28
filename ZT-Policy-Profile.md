# ZT-Policy-Profile

## 1. ZTA Component Definitions

### Policy Engine (PE)
The Policy Engine is the decision-making brain of a Zero Trust Architecture. It evaluates security signals such as user identity, device health, role, and network location to determine whether access to a protected resource should be granted or denied. The Policy Engine does not directly allow or block traffic—it makes the trust decision based on defined security policies.

### Policy Administrator (PA)
The Policy Administrator acts as the coordinator that applies the decision made by the Policy Engine. Once a decision is made, the Policy Administrator prepares the session and communicates the instructions to the enforcement systems. It ensures the access decision is properly executed.

### Policy Enforcement Point (PEP)
The Policy Enforcement Point is the gatekeeper between the user and the resource. It enforces the decision made by the Policy Engine by either allowing the connection to proceed or blocking it. The PEP does not make decisions; it only enforces them.

---

## 2. Core Principle Application

### Chosen Principle: Verify Explicitly

At the Golden State Water Treatment Facility, the HR Employee PII Database contains sensitive information such as background checks and certification records. The Policy Engine enforces the principle of Verify Explicitly by evaluating multiple real-time security signals before granting access.

For example, when an HR employee attempts to access the database, the Policy Engine verifies:

- The user's identity using multi-factor authentication (MFA).
- The user's role to confirm they are authorized HR personnel.
- The device posture to ensure it is company-managed, encrypted, and fully updated.
- The network context to confirm the connection is coming from an approved corporate VPN.

Only if all verification checks are satisfied does the Policy Engine approve access. This ensures that trust is based on explicit validation rather than assumption.

---

## 3. Simplified Policy Table

| Policy Requirement (Signal) | Condition to be Met by User | Action if Condition is Met |
|-----------------------------|-----------------------------|----------------------------|
| User Identity | User must authenticate with MFA and have authorized HR role privileges | Grant Access |
| Device Posture | Device must be company-managed, encrypted, and fully patched | Grant Access |
| Network Context | Connection must originate from approved corporate VPN within the United States | Grant Access |

---

## 4. Submission Details

# Git Repository Metadata

Filename: ZT-Policy-Profile.md  
Commit Message: Added Zero Trust Policy Profile for HR PII Database at Golden State Water Treatment Facility