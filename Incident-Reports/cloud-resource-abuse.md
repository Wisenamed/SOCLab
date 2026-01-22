# Incident Report: Cloud Resource Abuse

## Incident Summary
Anomalous Azure resource provisioning activity was detected, indicating potential misuse of cloud credentials and unauthorized resource creation.

---

## Incident Details
- Incident Type: Cloud Resource Abuse
- Severity: Medium
- Detection Source: Microsoft Sentinel
- Affected Platform: Microsoft Azure

---

## Detection Overview
The incident was detected through abnormal Azure Activity Logs showing unexpected virtual machine creation outside business hours.

---

## Affected Assets
- Azure subscription
- Cloud compute resources
- User account associated with provisioning

---

## Investigation Timeline
1. Alert triggered for unexpected resource creation
2. Analyst reviewed activity logs and user context
3. No approved change request found
4. Risk assessed as potential account misuse

---

## Indicators of Compromise (IOCs)
- VM creation events during non-business hours
- Elevated resource provisioning frequency
- Unfamiliar source IP for management actions

---

## Root Cause Analysis
The activity was consistent with compromised credentials being used to abuse cloud resources.

---

## Containment Actions
- Disabled affected user account
- Removed unauthorized resources
- Reviewed role assignments and permissions

---

## Remediation & Recommendations
- Enforce stricter RBAC controls
- Monitor cloud provisioning activity continuously
- Implement alerts for cost and usage anomalies

---

## Lessons Learned
- Cloud environments require identity-centric monitoring
- Early detection reduces financial and security impact
