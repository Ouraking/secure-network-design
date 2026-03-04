# Secure Network Design

A comprehensive secure network merger and implementation plan for integrating two companies with distinct regulatory requirements.

## Overview

This project addresses the challenge of securely merging networks for a financial company (Company A) acquiring a medical software provider (Company B). The design incorporates zero-trust principles, defense-in-depth controls, and cloud-based infrastructure while ensuring compliance with multiple regulatory frameworks.

## Key Deliverables

- **Network Merger Plan** — Risk-based integration strategy for combining two distinct network architectures
- **Vulnerability Assessment** — Identification and remediation of security gaps across both companies
- **Secure Network Topology** — Redesigned architecture implementing zero-trust and defense-in-depth
- **Cloud Migration Strategy** — Server migration to Microsoft Azure for scalability and redundancy
- **Compliance Framework** — Regulatory alignment with PCI-DSS, HIPAA, and GLBA

## Technical Highlights

### Infrastructure Upgrades
- Replaced end-of-life Cisco 7600 border routers with Cisco ASR 900
- Upgraded vulnerable Cisco Meraki MR 28 access points to MR 42
- Deployed Fortinet FortiGate FG 90G next-generation firewall
- Replaced Cisco 3750X switches (end-of-life) with Catalyst 1000-24P-4X-L

### Security Architecture
- **Zero-Trust Model** — No implicit trust; all access verified regardless of network location
- **Defense-in-Depth** — Multiple layered security controls across all OSI layers
- **Network Segmentation** — VLANs and firewall zones to isolate sensitive data
- **MFA Enforcement** — Multi-factor authentication across all access points
- **VPN (Cisco AnyConnect)** — Secure remote access for distributed workforce

### Cloud Migration
- All servers migrated to Microsoft Azure cloud services
- Eliminated legacy Windows Server 2012 and obsolete operating systems
- Achieved scalability, elasticity, and disaster recovery capabilities
- Approximate annual cost: $19,075

### Compliance Coverage
| Framework | Scope |
|-----------|-------|
| **PCI-DSS** | Credit card payment processing (Company B) |
| **HIPAA** | Medical provider data protection (Company B) |
| **GLBA** | Financial data protection (Company A) |

## Budget Summary

Total first-year budget: **$50,000**

| Item | Cost |
|------|------|
| Cisco ASR 900 Routers (x2) | $4,200 |
| Cisco Catalyst 1000 Switch | $1,295 |
| Cisco MR 42 Access Points (x2) | $900.88 |
| Fortinet FortiGate FG 90G | $2,150 |
| Microsoft Azure Migration | $19,075/yr |
| Cisco AnyConnect VPN | Included |

## Technologies & Tools

- **Firewalls:** Fortinet FortiGate NGFW, Sophos XG
- **Networking:** Cisco ASR 900, Catalyst 1000, AnyConnect VPN
- **Cloud:** Microsoft Azure
- **Access Points:** Cisco Meraki MR 42
- **Security Controls:** MFA, IDS/IPS, SIEM, DLP

## Network Diagram

The merged network topology features:
- Dual ISP connections for redundancy
- Fortinet and Sophos firewalls in layered configuration
- Azure cloud hosting for all server workloads
- Segmented zones for Company A and Company B assets
- MFA enforcement at all critical access points

## Author

**Koffi Jean-Marie Amedjonekou**
Security Researcher

## License

This project is shared for educational and portfolio purposes.
