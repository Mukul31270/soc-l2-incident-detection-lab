# SOC L2 Lab Architecture

This directory documents the architecture and communication flow of the SOC L2 Incident Detection & Investigation Lab.

## Components

- Kali Linux — Attacker / Analyst
- Windows 11 — Endpoint
- Wazuh — SIEM / EDR
- Sysmon — Windows telemetry

## Network

Kali → Windows 11 → Wazuh Manager

All attack simulations are performed inside the isolated lab environment.
