# SOC Home Lab – Anomalous Login & Account Compromise Detection

## Overview

This project simulates a real-world Security Operations Center (SOC) scenario focused on detecting and investigating a potential account compromise.

The lab demonstrates how anomalous login behavior combined with endpoint activity can indicate unauthorized access.

---

## Objectives

* Detect anomalous login behavior
* Analyze multi-source logs (network + endpoint)
* Perform manual event correlation
* Build a structured incident investigation

---

## Lab Architecture

* **Attacker Machine:** Ubuntu
* **Victim Machine:** Windows 10 (Sysmon + Suricata + Wazuh Agent)
* **SIEM:** Wazuh Server (Ubuntu)

---

## Technologies Used

* Wazuh
* Sysmon
* Suricata
* FreeRDP

---

## Attack Scenario

1. Normal user activity (baseline)
2. Remote login via RDP from an unusual IP
3. Immediate execution of PowerShell
4. System reconnaissance commands executed
5. User creation

---

## Detection Approach

The detection was based on identifying deviations from normal behavior:

* Local login vs Remote login (RDP)
* Known vs Unknown IP
* No activity vs Immediate command execution

---

## Key Findings

* Anomalous RDP login detected (Logon Type 10)
* Source IP not part of normal behavior (192.168.56.103)
* PowerShell execution immediately after login
* Commands consistent with reconnaissance
* User creation

---

## Timeline

- 05:49 PM: Normal login (baseline)
- 08:16 PM: Remote login from unknown IP
- 08:17 PM: PowerShell execution
- 08:18 PM: System enumeration

---

## MITRE ATT&CK Mapping

* T1078 – Valid Accounts
* T1059 – Command Execution

---

## Results

The analysis indicates a high probability of account compromise due to:

* Strange behavior in login pattern
* Post-authentication activity consistent with attacker behavior

---
