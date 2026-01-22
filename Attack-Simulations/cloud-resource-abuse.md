# Attack Simulation: Cloud Resource Abuse

## Objective
Simulate abuse of cloud credentials to provision unauthorized resources in Azure.

---

## Attack Scenario
An attacker uses compromised credentials to create cloud resources for malicious or unauthorized purposes.

---

## Simulated Attacker Actions
- Virtual machine creation
- Resource provisioning outside business hours
- Use of elevated permissions

---

## Observed Telemetry
- Azure Activity Logs
- Sentinel alerts
- Abnormal resource creation patterns

---

## SOC Visibility
- Detection of unexpected cloud activity
- Identity-focused investigation
- Correlation with authentication events

---

## Defensive Outcome
- Unauthorized resources removed
- Credentials disabled
- RBAC controls reviewed
