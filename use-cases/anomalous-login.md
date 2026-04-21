# Use Case: Anomalous Login Detection

## Objective
Detect suspicious account access based on unusual login behavior.

## Detection Criteria
- Remote login (RDP Logon Type 10)
- Unusual source IP
- Deviation from normal login patterns

## Data Sources
- Windows Security Logs
- Sysmon
- Suricata Logs

## MITRE ATT&CK
- T1078 – Valid Accounts
