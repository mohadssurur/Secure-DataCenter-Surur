# Secure Data Center — Surur Trading and Contracting Company

## Project Overview
This repository contains the configuration files and implementation details for the secure data center developed for Surur Trading and Contracting Company as part of a Computer Engineering graduation project specialising in Cybersecurity at Middle East College.

## Project Objective
To design and implement a secure, multi-layered data center infrastructure that protects the confidentiality, integrity, and availability of company data using industry-standard security tools and frameworks.

## Security Components
| Component | Tool | Version |
|---|---|---|
| Firewall | pfSense | 2.7.2 |
| IDS/IPS | Suricata | 7.x |
| VPN | OpenVPN | 2.6 |
| SIEM | Wazuh | 4.7.5 |
| Hypervisor | VirtualBox | 7.x |
| Network Simulator | GNS3 | 2.2.x |

## Network Design
- 3-Tier Architecture (Core, Distribution, Access)
- 6 VLANs (Management, Servers, Users, DMZ, Security, VPN)
- DMZ for public-facing services
- Defence-in-depth security strategy

## Standards Compliance
- ISO/IEC 27001:2022
- NIST SP 800-53 Rev. 5
- TIA-942 Data Center Standard

## Author
- Student: Mohads
- Institution: Middle East College
- Department: Computing and Electronics Engineering
- Academic Year: 2025-2026
