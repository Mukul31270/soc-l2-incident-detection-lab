# INC-002 — Account Creation & Failed Authentication

## Incident Overview

| Field | Value |
|---|---|
| Incident ID | INC-002 |
| Severity | High |
| Host | WIN11-SOC-LAB |
| Status | Investigated |
| Environment | Controlled SOC Lab |

## Detection

Two related Windows security events were observed:

- Rule 60109 — User account enabled or created
- Rule 60122 — Logon Failure / bad password

## Analysis

A new local Windows account was created during the controlled
laboratory simulation. A failed authentication attempt was then
generated against the endpoint.

Account creation can be associated with persistence, while
repeated or suspicious authentication failures can indicate
credential attacks.

The events were correlated in Wazuh using Windows Security
telemetry.

## MITRE ATT&CK

- T1136.001 — Create Account: Local Account
- T1110 — Brute Force

## Evidence

- Wazuh Rule 60109
- Wazuh Rule 60122
- Windows Security event telemetry
- Endpoint: WIN11-SOC-LAB

## IOC Assessment

No malicious external IOC was identified.

The activity was intentionally generated for this controlled lab.

## Analyst Conclusion

The combination of account creation and failed authentication
represents suspicious account-management activity.

The activity was confirmed as a controlled laboratory simulation,
with no real compromise.

## Recommended Response

1. Verify whether the account creation was authorized.
2. Review account and group membership changes.
3. Investigate the source of failed authentication.
4. Disable unauthorized accounts.
5. Review surrounding endpoint events.
6. Monitor for repeated authentication failures.
