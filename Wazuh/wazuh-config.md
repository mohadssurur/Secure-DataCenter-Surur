# Wazuh SIEM Configuration
## Secure Data Center — Surur Trading and Contracting Company

## Overview
Wazuh 4.7.5 is deployed as the centralised SIEM platform on the Security VLAN (VLAN 50).
It provides log aggregation, event correlation, threat detection, and compliance monitoring.

## Deployment Details
| Setting | Value |
|---|---|
| Version | 4.7.5 |
| OS | Ubuntu Server 24.04 LTS |
| IP Address | 192.168.50.11 |
| VLAN | Security (VLAN 50) |
| Web Interface | https://127.0.0.1:8443 |
| Default User | admin |

## Log Sources
| Source | Type |
|---|---|
| pfSense | Firewall logs |
| Suricata | IDS/IPS alerts |
| OpenVPN | VPN connection logs |
| Ubuntu Server | System logs |
| File Server | Access logs |

## Active Modules
- Security Events
- Integrity Monitoring
- Policy Monitoring
- System Auditing
- Vulnerability Detection
- MITRE ATT&CK
- NIST 800-53 Compliance
- PCI DSS Compliance

## Integration
- Receives logs from all network components via Wazuh agents
- Correlates Suricata alerts with system events
- Generates automated alerts for suspicious activity
- Provides compliance dashboards for ISO 27001 and NIST 800-53
