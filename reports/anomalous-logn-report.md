# Incident Report – Anomalous Login

## Incident Type
Account Compromise

## Severity
High

## Summary
An anomalous login was detected from an unusual IP address, followed by suspicious command execution.

---

## Key Indicators

- Remote login (RDP)
- Unknown source IP
- PowerShell execution

---

## Risk Assessment

Probability: High  
Impact: High  
Confidence: High  

---

## MITRE ATT&CK

- T1078 – Valid Accounts
- T1059 – Command Execution

---

## Recommendations

- Reset affected credentials
- Enable MFA
- Monitor remote access activity
- Restrict RDP access
