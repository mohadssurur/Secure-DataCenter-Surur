# OpenVPN Configuration
## Secure Data Center — Surur Trading and Contracting Company

## Overview
OpenVPN 2.6 is deployed as the remote access VPN server on the WAN interface.
It provides encrypted remote access for authorised users using certificate-based authentication.

## Server Configuration
| Setting | Value |
|---|---|
| Interface | WAN |
| Protocol | UDP4 |
| Port | 1194 |
| Tunnel Network | 192.168.60.0/24 |
| Local Network | 192.168.20.0/24 |
| Encryption | AES-256-GCM |
| Auth Digest | SHA256 |
| DH Parameters | 4096 bits |
| TLS Version | 1.3 |

## Certificate Authority
| Setting | Value |
|---|---|
| CA Name | Surur-CA |
| Key Length | 4096 bits |
| Lifetime | 3650 days |
| Country | OM |
| Organisation | Surur Trading and Contracting |

## Security Features
- Certificate-based authentication
- Split tunnelling disabled
- All remote traffic routed through VPN
- Concurrent connections limit: 10
- Dynamic IP retention enabled
