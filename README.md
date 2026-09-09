# SOC L2 Incident Detection & Investigation Lab

I designed and implemented this hands-on Security Operations Center (SOC) lab to practice real-world incident detection, alert triage, endpoint investigation, MITRE ATT&CK mapping, IOC extraction, and incident documentation.

The lab simulates a small SOC environment using Kali Linux as the attacker/analyst system, Windows 11 as the monitored endpoint, Sysmon for endpoint telemetry, and Wazuh for centralized security monitoring and detection.

## What I Implemented

- Designed the SOC lab architecture
- Deployed and configured Wazuh
- Configured a Windows 11 endpoint with Wazuh Agent
- Integrated Sysmon endpoint telemetry
- Generated controlled security events in an isolated lab
- Analyzed Wazuh alerts and endpoint telemetry
- Investigated suspicious activity
- Mapped detections to MITRE ATT&CK
- Extracted indicators of compromise (IOCs)
- Documented incident investigations and findings

## Detection Scenarios

1. Suspicious PowerShell Execution — MITRE T1059.001
2. Network Discovery — MITRE T1046
3. Failed Authentication — MITRE T1110
4. Account Creation — MITRE T1136
5. Scheduled Task Persistence — MITRE T1053.005

## Investigation Workflow

Attack Simulation → Telemetry Collection → Wazuh Detection → Alert Triage → Investigation → MITRE ATT&CK Mapping → IOC Extraction → Incident Documentation

## Key Skills Demonstrated

- SIEM Monitoring
- Wazuh
- Windows Security Monitoring
- Sysmon
- Alert Triage
- Incident Investigation
- Detection Analysis
- MITRE ATT&CK
- IOC Extraction
- Endpoint Telemetry
- Security Documentation
