# INC-001 — Suspicious PowerShell Execution

## Incident Overview

| Field | Value |
|---|---|
| Incident ID | INC-001 |
| Severity | High |
| Host | WIN11-SOC-LAB |
| Detection | Suspicious PowerShell Execution |
| Wazuh Rule | 92057 |
| MITRE ATT&CK | T1059.001 |
| Status | Investigated |
| Environment | Controlled SOC Lab |

## Alert

Wazuh detected a PowerShell process spawning another PowerShell
process that executed a Base64-encoded command.

## Investigation

The activity was generated intentionally as part of a controlled
security laboratory exercise.

The use of encoded PowerShell is suspicious because command
encoding can be used to obfuscate PowerShell activity and make
commands less immediately visible during investigation.

Sysmon process telemetry provided the process execution evidence,
while Wazuh correlated the activity and generated a high-severity
alert.

## MITRE ATT&CK

**T1059.001 — Command and Scripting Interpreter: PowerShell**

## Evidence

- Wazuh Rule: 92057
- Severity: Level 12
- Sysmon process execution telemetry
- Base64-encoded PowerShell command
- Endpoint: WIN11-SOC-LAB

## IOC Assessment

No malicious external IOC was identified.

The encoded command was intentionally generated for this lab.

## Analyst Conclusion

The alert represents suspicious PowerShell execution and was
successfully detected by Wazuh.

The activity was confirmed as a controlled laboratory simulation
and not a real compromise.

## Recommended Response

1. Review the PowerShell command.
2. Decode and analyze encoded content.
3. Investigate parent/child process relationships.
4. Review surrounding network activity.
5. Check for persistence mechanisms.
6. Isolate the endpoint if malicious execution is confirmed.
