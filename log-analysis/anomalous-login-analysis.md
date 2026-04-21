# Anomalous Login Analysis

## Overview
A suspicious remote login was identified, followed by immediate command execution activity.

---

## Baseline Behavior

Normal activity observed:
- Local login (Logon Type 2)
- No immediate command execution
- During normal business hours

---

## Suspicious Activity

### Remote Login
- Event ID: 4624
- Logon Type: 10 (RDP)
- Source IP: [192.168.56.103]
- Outside of regular hours

---

### Post-Login Activity
- PowerShell execution detected
- Commands:
  - whoami
  - ipconfig
  - net user
  - user creation

---

## Timeline

- T0: Normal login (baseline)
- T1: Remote login from unknown IP
- T2: PowerShell execution
- T3: System enumeration

---

## Analysis

The login deviates from normal behavior due to:
- Remote access via RDP
- Unknown source IP
- Immediate execution of commands
- outside of regular hours

---

## Conclusion

This activity is consistent with unauthorized access using valid credentials.
