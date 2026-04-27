# pfSense Firewall Configuration
## Secure Data Center — Surur Trading and Contracting Company

## Overview
pfSense 2.7.2 is deployed as the primary firewall and gateway for the secure data center.
It enforces zone-based traffic filtering across all six VLANs using a default-deny policy.

## VLAN Interfaces
| Interface | VLAN ID | IP Address | Description |
|---|---|---|---|
| em1.10 | 10 | 192.168.10.1/24 | Management |
| em1.20 | 20 | 192.168.20.1/24 | Servers |
| em1.30 | 30 | 192.168.30.1/24 | Users |
| em1.40 | 40 | 192.168.40.1/24 | DMZ |
| em1.50 | 50 | 192.168.50.1/24 | Security |
| em1.60 | 60 | 192.168.60.1/24 | VPN |

## Firewall Rules Summary

### DMZ (VLAN 40)
- Allow TCP port 80 (HTTP) from Internet to DMZ
- Allow TCP port 443 (HTTPS) from Internet to DMZ
- Allow TCP port 25 (SMTP) from Internet to DMZ
- Block all traffic from DMZ to Internal LAN

### Users (VLAN 30)
- Allow TCP port 80 (HTTP) to Internet
- Allow TCP port 443 (HTTPS) to Internet
- Allow TCP port 445 to Servers VLAN
- Block access to Management VLAN

### Management (VLAN 10)
- Block TCP port 23 (Telnet) — all interfaces
- Allow TCP port 22 (SSH) — admin access only
- Allow full access to all network devices

### VPN (VLAN 60)
- Allow TCP port 445 to Servers VLAN
- Allow TCP port 80 to Internet
- Allow TCP port 443 to Internet

### Default Policy
- Deny all traffic not matched by explicit allow rules
