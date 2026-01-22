# Privileged Account Activity Monitoring

## Objective
Monitor and detect suspicious activity involving privileged or administrative accounts across on-premise and cloud environments.

---

## Threat Description
Privileged accounts are high-value targets. Unauthorized use or changes can lead to full environment compromise.

---

## Data Sources
- Windows Security Event Logs
- Azure AD (Entra ID) Audit Logs
- Microsoft Sentinel
- SIEM (Splunk)

---

## Detection Logic

### On-Prem Privileged Activity
- Monitor changes to local or domain administrator groups
- Detect logins by privileged accounts from unusual sources

### Cloud Privileged Activity
- Monitor Azure AD role assignment changes
- Detect elevated role usage outside normal patterns
- Identify failed or risky sign-ins involving privileged accounts

---

## MITRE ATT&CK Mapping
- T1078 – Valid Accounts
- T1098 – Account Manipulation

---

## SOC Investigation Steps
1. Identify affected privileged account
2. Review role assignment or group membership changes
3. Validate whether activity was authorized
4. Review authentication and session history
5. Assess potential impact

---

## Response Actions
- Revoke unauthorized role assignments
- Reset credentials for affected accounts
- Enforce or validate MFA
- Escalate incident due to elevated risk

---

## Escalation Criteria
- Administrator or global roles involved
- Multiple privileged accounts affected
- Evidence of unauthorized role changes

---

## Notes
Privileged account activity requires immediate attention due to potential enterprise-wide impact.
