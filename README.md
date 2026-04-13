# Secure Network Design

A comprehensive secure network merger and implementation plan for integrating two companies with distinct regulatory requirements.

## Overview

This project addresses the challenge of securely merging networks for a financial company (Company A) acquiring a medical software provider (Company B). The design incorporates zero-trust principles, defense-in-depth controls, and cloud-based infrastructure while ensuring compliance with multiple regulatory frameworks.

## Key Deliverables

- **Network Merger Plan:** Risk-based integration strategy for combining two distinct network architectures
- **Vulnerability Assessment:** Identification and remediation of security gaps across both companies
- **Secure Network Topology:** Redesigned architecture implementing zero-trust and defense-in-depth
- **Cloud Migration Strategy:** Server migration to Microsoft Azure for scalability and redundancy
- **Compliance Framework:** Regulatory alignment with PCI-DSS, HIPAA, and GLBA

## Technical Highlights

### Infrastructure Upgrades
- Replaced end-of-life Cisco 7600 border routers with Cisco ASR 900
- Upgraded vulnerable Cisco Meraki MR 28 access points to MR 42
- Deployed Fortinet FortiGate FG 90G next-generation firewall
- Replaced Cisco 3750X switches (end-of-life) with Catalyst 1000-24P-4X-L

### Security Architecture
- **Zero-Trust Model:** No implicit trust; all access verified regardless of network location
- **Defense-in-Depth:** Multiple layered security controls across all OSI layers
- **Network Segmentation:** VLANs and firewall zones to isolate sensitive data
- **MFA Enforcement:** Multi-factor authentication across all access points
- **VPN (Cisco AnyConnect):** Secure remote access for distributed workforce

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

## Key Decision Rationale

### Why Fortinet FortiGate over alternatives?
The FortiGate FG 90G was selected over Palo Alto PA-440 and Cisco Firepower 1010 for three reasons: (1) **unified threat management** — FortiGate consolidates firewall, IPS, antivirus, and web filtering into a single appliance, reducing operational complexity during a high-risk merger transition; (2) **cost-to-performance ratio** — at $2,150, the FG 90G delivers enterprise-grade NGFW capabilities at roughly half the cost of comparable Palo Alto units; (3) **FortiGuard integration** — threat intelligence feeds update in real-time without requiring a separate subscription tier.

### Why Azure over AWS for this use case?
Azure was chosen because Company B (medical software provider) already operated Microsoft 365 for email and productivity. Azure Active Directory integration provided **single-pane-of-glass identity management** across on-premises and cloud resources — critical during a merger where two identity systems must be consolidated. AWS would have required additional identity federation tooling and licensing.

### Why Zero Trust for a merger scenario?
During a network merger, implicit trust boundaries are the highest-risk factor. Neither company's existing trust model can be assumed valid for the combined entity. Zero Trust eliminates this by requiring **explicit verification for every access request**, regardless of whether it originates from Company A or Company B's legacy network. This approach prevented the need to audit and reconcile two separate trust models.

### Why dual-firewall layering (Fortinet + Sophos)?
Defense-in-depth mandates that no single vendor's vulnerability can compromise the entire perimeter. By layering Fortinet (perimeter) with Sophos XG (internal segmentation), an exploit targeting one vendor's firmware or signature engine cannot bypass the second layer. This is a deliberate architectural choice aligned with NIST SP 800-53 SC-7 (Boundary Protection).

## Lessons Learned

- **Inventory before architecture:** The vulnerability assessment revealed end-of-life equipment (Cisco 7600, Windows Server 2012) that would have silently undermined the new security controls. A full asset inventory must precede any design work.
- **Compliance drives budget conversations:** Framing the $50K budget around PCI-DSS, HIPAA, and GLBA non-compliance penalties made executive approval straightforward. Security spending is easier to justify when tied to regulatory risk.
- **VPN is not optional in mergers:** Distributed workforces from both companies needed secure access from day one. Deploying Cisco AnyConnect early in the timeline prevented shadow IT workarounds that would have created unmonitored access paths.
- **Cloud migration simplifies EOL remediation:** Rather than replacing Windows Server 2012 with new on-premises hardware, migrating to Azure eliminated the OS patching burden entirely and shifted responsibility to Microsoft's shared responsibility model.

## Skills Demonstrated

`Zero Trust Architecture` `Defense-in-Depth` `Network Segmentation` `Vulnerability Assessment` `Cloud Migration (Azure)` `Firewall Configuration (Fortinet/Sophos)` `Regulatory Compliance (PCI-DSS, HIPAA, GLBA)` `Risk-Based Budgeting` `Infrastructure Lifecycle Management` `VPN Deployment`

## Author

**Koffi Jean-Marie Amedjonekou**
Cybersecurity Engineer

## License

This project is shared for educational and portfolio purposes.
