# SOC Runbook: Brute Force Authentication Response

## Purpose
This runbook provides step-by-step guidance for SOC analysts to respond to suspected brute force or password spray authentication attacks.

---

## Trigger Conditions
This runbook should be followed when one or more of the following alerts are generated:
- Multiple failed authentication attempts from a single source
- Failed login attempts across multiple user accounts
- Azure AD risky sign-in or password spray alerts

---

## Data Sources
- Windows Security Event Logs (Event ID 4625)
- Azure AD (Entra ID) Sign-In Logs
- SIEM alerts (Splunk / Microsoft Sentinel)

---

## Initial Triage
1. Review alert details and confirm detection logic
2. Identify source IP address(es)
3. Identify targeted user account(s)
4. Check alert frequency and time window

---

## Investigation Steps
1. Review authentication logs for successful logins following failures
2. Validate geolocation and device information
3. Check historical login behavior for affected accounts
4. Review IP reputation using threat intelligence sources
5. Determine if activity is malicious or user-generated error

---

## Containment Actions
- Temporarily block or restrict suspicious source IPs
- Force password reset for affected user accounts
- Revoke active sessions (cloud identity)
- Enable or validate Multi-Factor Authentication (MFA)

---

## Escalation Criteria
Escalate the incident to higher-level response if:
- Successful login occurred after failed attempts
- Privileged or administrator accounts are involved
- Multiple users are affected
- Repeated attacks persist after initial containment

---

## Recovery Actions
- Restore normal access for affected users after validation
- Monitor accounts for recurring suspicious activity
- Confirm security controls are functioning as expected

---

## Post-Incident Activities
- Document incident findings and actions taken
- Update detection thresholds if required
- Identify gaps in authentication controls
- Recommend security improvements

---

## Notes
This runbook is intended for use in SOC and MSSP environments and should be adapted based on organizational policies and risk tolerance.
