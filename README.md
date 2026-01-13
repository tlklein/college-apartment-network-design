# College Apartment Network Design Project

## Project Overview

This project designs a scalable, secure, and resilient network for a multi-unit college apartment complex. The architecture applies enterprise network principles (layered routing, VLAN segmentation, and SD-WAN) to support thousands of concurrent users, high-bandwidth multimedia, online learning, and IoT devices while preserving management simplicity through cloud-based tooling.

### Problem

Residential multi-tenant environments often suffer from poor Wi-Fi coverage, noisy broadcast domains, insecure device mixing (guest vs. staff vs. IoT), and operational complexity when scaling.

### Solution

A hotel-style, multi-tier network that separates traffic by purpose (resident, guest, staff, IoT), uses Cisco Meraki cloud management and SD-WAN for resilient WAN connectivity, and specifies enterprise hardware for wired/wireless performance and future growth.

### Tech

Network Hardware & Management

- Cisco Meraki (MR access points, MX security/SD-WAN appliances, MS/Catalyst switches)
- Router/Firewall: MX250 (SD-WAN, security)
- Core/Distribution: C9300 / C9500 class switches (Ethernet fabric & routing)
- Access Points: MR53, MR30H (high density + hospitality)

Design Patterns

- VLAN segmentation, Layer-2/Layer-3 access
- DHCP scope planning, NAT, and per-VLAN ACLs
- Channel planning (1/6/11), band steering, and QoS for multimedia
- Monitoring: cloud dashboards + SNMP/export to third-party observability

## Result / Key Deliverables

- Complete multi-floor logical and physical network diagrams (per floor topology).  
- VLAN, IP addressing plan, and DHCP/NAT configuration patterns.  
- Hardware & licensing bill of materials (BOM) with cost estimates.  
- Operational playbook: onboarding, guest provisioning, firmware/patch plan, failover procedures.  
- Security & segmentation plan including RBAC and least-privilege management.

## Scope & Features

- Layered Architecture: Core → Distribution → Access for redundancy and predictable routing.  
- VLAN Segmentation: Resident, Guest, Staff, IoT, Management, and Services VLANs with ACLs.  
- High-Density Wi-Fi: MR53 + MR30H placements and channel plan, MIMO considerations, and capacity planning.  
- SD-WAN Resilience: MX appliances for active/active internet links and centralized policy enforcement.  
- Operational Management: Cisco Meraki cloud console for zero-touch provisioning, telemetry, and alerting.  
- Cost Analysis: BOM including devices, SFPs, cabling, mounting, and Meraki licensing tiers.

## Diagrams

Diagrams provide the main artifacts for reviewers. Each figure includes a brief caption explaining intent. See the 'Network  Design' PDF for further details.

### First Floor - Common Areas & Lobby

![First Floor Diagram](/diagrams/diagram-3.png)  
Caption: Public area AP placement, guest onboarding flow, and primary MX uplink aggregation.

### Second Floor - Residential Pod 1

![Second Floor Diagram](/diagrams/diagram-2.png)  
Caption: Access switch layout, resident VLANs, and local trunking to distribution switches.

### Third–Eighth Floors - Typical Pod Design

![Upper Floors Diagram](/diagrams/diagram-1.png)  
Caption: Repeating pod topology, AP density, and uplink consolidation strategy.

## Cost Summary (high level)

- Hardware: MX250 (edge), C9300/C9500 switches, MR53/MR30H APs.  
- Licensing: Meraki licensing per device (MBU/enterprise tiers).  

## Documentation & Deliverables

- `diagrams/` - floor diagrams and ER-style topology images.  
- `docs/` - full report covering estimated costs, recommendations, and reasoning.

## Repo Structure

```text
├── diagrams/
│   ├── diagram-1.png
│   ├── diagram-2.png
│   └── diagram-3.png
├── docs/
│   ├── Network_Design.pdf
│   └── Floor_Plan.vsdx
└── README.md
