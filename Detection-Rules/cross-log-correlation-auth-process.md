# Cross-Log Correlation: Authentication and Process Activity

## Objective
Reduce false positives by correlating authentication anomalies with suspicious process execution.

---

## Threat Description
Single alerts may appear benign in isolation. Correlating authentication events with endpoint behavior improves detection accuracy.

---

## Data Sources
- Windows Security Logs
- Sysmon Process Creation Logs
- SIEM (Splunk)

---

## Detection Logic
- Identify abnormal authentication behavior
- Correlate with PowerShell or LOLBin execution on the same host
- Trigger alert only when both conditions are met

---

## MITRE ATT&CK
- T1078 – Valid Accounts
- T1059 – Command and Scripting Interpreter

---

## SOC Investigation Steps
1. Review authentication anomaly
2. Validate correlated process execution
3. Assess likelihood of compromise
4. Decide escalation or closure

---

## Notes
Correlation reduces alert fatigue and improves SOC efficiency.
