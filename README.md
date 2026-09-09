# SOC L2 Incident Detection & Investigation Lab

A hands-on Security Operations Center (SOC) lab built with Wazuh, Windows 11, Sysmon, and Kali Linux.

## Architecture

- Kali Linux — Attacker / Analyst
- Windows 11 — Monitored Endpoint
- Wazuh — SIEM / XDR
- Sysmon — Endpoint Telemetry

## Detection Scenarios

1. Suspicious PowerShell Execution — MITRE T1059.001
2. Network Discovery — MITRE T1046
3. Failed Authentication — MITRE T1110
4. Account Creation — MITRE T1136
5. Scheduled Task Persistence — MITRE T1053.005

## Investigation Workflow

Attack Simulation → Telemetry → Wazuh Alert → Triage → Investigation → MITRE Mapping → IOC Extraction → Incident Report

## Objective

This project demonstrates practical SOC L2 capabilities including alert analysis, endpoint investigation, detection engineering, MITRE ATT&CK mapping, IOC extraction, and incident documentation.

## Lab Environment

| Component | Role |
|---|---|
| Kali Linux | Attacker / Analyst |
| Windows 11 | Victim Endpoint |
| Wazuh | SIEM / Detection |
| Sysmon | Endpoint Telemetry |
