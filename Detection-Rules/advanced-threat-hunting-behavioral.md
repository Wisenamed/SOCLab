# Advanced Threat Hunting: LOLBins, Insider, and Persistence Patterns

## Objective
Detect advanced threats using behavioral indicators rather than single-event alerts.

---

## Threat Description
Advanced attackers and malicious insiders operate slowly, blending into normal activity using native tools (LOLBins).

---

## Data Sources
- Windows Security Logs
- Sysmon Process Execution Logs
- SIEM (Splunk)

---

## Detection Logic

### LOLBins Monitoring
- Detect execution of certutil, rundll32, mshta
- Flag unusual command-line arguments

### Insider Threat Indicators
- Abnormal access outside business hours
- Access to systems unrelated to user role

### Low-and-Slow Persistence
- Repeated low-frequency activity over extended time periods
- Patterns that evade threshold-based alerts

---

## MITRE ATT&CK
- T1218 – Signed Binary Proxy Execution
- T1078 – Valid Accounts
- T1036 – Masquerading

---

## SOC Investigation Steps
1. Review historical activity timelines
2. Compare behavior against baseline
3. Validate user role and access necessity
4. Escalate if intent appears malicious

---

## Notes
These detections are threat-hunting focused and require analyst judgment.
