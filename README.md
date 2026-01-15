# AWS IAM Enumeration CTF – Security Assessment using PwnedLabs

## Overview
This repository documents a **Capture-the-Flag (CTF) style AWS IAM security assessment** focused on enumerating identity permissions, analyzing policy misconfigurations, and validating potential data exposure and privilege escalation risks.

The exercise simulates a realistic scenario where a compromised IAM user is investigated to determine:
- What permissions they possess
- Which cloud resources can they access
- Whether misconfigurations allow unintended or excessive access

A flag is used as a **controlled proof-of-access artifact** to confirm impact once security weaknesses are identified.

All activities were conducted in a **sandboxed training environment** designed for defensive security learning.

---

## Objectives
The goals of this assessment were to:

- Enumerate IAM users, groups, roles, and attached policies
- Analyze effective permissions and their security implications
- Identify accessible AWS resources and potential data exposure
- Assess risks such as excessive permissions or privilege escalation paths
- Validate findings using a CTF-style flag as proof of impact
- Propose actionable mitigations aligned with least-privilege principles

---

## Scope & Methodology
- **Cloud Platform:** Amazon Web Services (AWS)
- **Access Model:** Pre-issued IAM credentials for a simulated compromised user
- **Approach:**
  - AWS CLI–based enumeration
  - Policy and permission analysis
  - Targeted resource inspection
  - Minimal, non-destructive validation of access


---

## High-Level Assessment Flow
1. Configure and verify AWS CLI credentials
2. Identify the compromised IAM identity
3. Enumerate attached and inherited IAM policies
4. Analyze effective permissions and risk exposure
5. Identify accessible services and resources
6. Validate impact by retrieving a flag
7. Document findings and propose mitigations

---

## Proof of Impact (CTF Flag)
The flag represents a **deliberately placed indicator** used to confirm that excessive permissions could lead to unauthorized data access.

## Key Findings (Summary)
- Excessive IAM permissions increased blast radius
- Policy design allowed broader access than required
- Certain permissions enabled access to sensitive resources
- Lack of strict least-privilege enforcement increased risk

Detailed findings and command outputs are documented in the accompanying report.


## Mitigation Recommendations
- Enforce least-privilege IAM policies
- Use role-based access instead of long-lived users
- Restrict sensitive permissions (e.g., Secrets Manager access)
- Apply permission boundaries and service control policies
- Continuously audit IAM permissions and usage patterns

# Redaction
-All AWS access keys referenced in this assessment were short-lived, lab-issued credentials provided by a controlled training environment.
-Credentials were temporary and automatically expired when the lab session ended
-Keys were scoped to a simulated AWS account, not a production environment
-No long-lived access keys were created, stored, or reused

## Author
Kalpesh Parmar  
Cloud & Application Security  
AWS IAM • Access Control • Least Privilege








