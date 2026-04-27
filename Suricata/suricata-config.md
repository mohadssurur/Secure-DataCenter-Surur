# Suricata IDS/IPS Configuration
## Secure Data Center — Surur Trading and Contracting Company

## Overview
Suricata 7.x is deployed in inline IPS mode on the LAN interface (em1).
It provides real-time intrusion detection and prevention using the OISF Emerging Threats Open ruleset.

## Deployment Details
| Setting | Value |
|---|---|
| Interface | LAN (em1) |
| Mode | Inline IPS |
| Blocking Mode | Enabled |
| Pattern Match | AUTO |
| Ruleset | OISF Emerging Threats Open |

## Detected Threat Categories
- Port scanning
- Denial of Service (DoS)
- Brute force attacks
- Man-in-the-Middle (MITM)
- SQL injection
- Malware traffic

## Integration
- Suricata alert logs are forwarded to Wazuh SIEM for centralised correlation
- Alerts trigger automated responses via Wazuh active response module

## Key Settings
- Hardware checksum offloading: Disabled
- Hardware TCP segmentation offloading: Disabled
- Hardware large receive offloading: Disabled
