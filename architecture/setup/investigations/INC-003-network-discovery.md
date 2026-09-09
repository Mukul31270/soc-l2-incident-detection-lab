# INC-003 — Network Discovery Activity

## Incident Overview

| Field | Value |
|---|---|
| Incident ID | INC-003 |
| Severity | Medium |
| Host | WIN11-SOC-LAB |
| Status | Investigated |
| Environment | Controlled SOC Lab |

## Detection

Network discovery commands were executed on the Windows endpoint:

- `ipconfig /all`
- `arp -a`
- `netstat -ano`

## Analysis

The commands were used to enumerate network configuration,
ARP information, and active network connections.

These utilities are legitimate administrative tools, but similar
activity can be used by an attacker during reconnaissance after
obtaining access to an endpoint.

## MITRE ATT&CK

- T1016 — System Network Configuration Discovery
- T1046 — Network Service Scanning

## Evidence

- Windows endpoint telemetry
- Wazuh Threat Hunting events
- Host: WIN11-SOC-LAB
- Network discovery commands executed during controlled testing

## IOC Assessment

No malicious external IP address or domain was identified.

The activity was intentionally generated for this laboratory.

## Analyst Conclusion

Network reconnaissance activity was successfully generated and
observed through the endpoint telemetry pipeline.

The activity was confirmed as a controlled lab simulation.

## Recommended Response

1. Identify the initiating user and process.
2. Correlate with preceding PowerShell/process events.
3. Review network connections.
4. Investigate unexpected reconnaissance activity.
5. Monitor for subsequent lateral-movement behavior.
