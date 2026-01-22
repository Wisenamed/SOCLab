# Azure AD Risky Sign-In Detection

## Objective
Detect potentially compromised accounts using Azure AD sign-in risk indicators and anomalous login behavior.

---

## Data Sources
- Azure AD (Entra ID) Sign-In Logs
- Microsoft Sentinel

---

## Detection Logic
- Identify sign-ins flagged as high or medium risk
- Detect impossible travel scenarios
- Monitor sign-ins from unfamiliar devices or locations

---

## MITRE ATT&CK
- T1078 – Valid Accounts

---

## SOC Investigation Steps
1. Review sign-in details and risk level
2. Validate user location and device information
3. Check for MFA challenges or failures
4. Review recent account activity

---

## Response Actions
- Force password reset
- Revoke active sessions
- Enforce MFA
- Monitor account post-remediation
