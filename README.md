# College Apartment Network Design Project

## Project Overview

This project covers a scalable, secure, and resilient network for a multi-unit college apartment complex. It applies enterprise network principles (layered routing, VLAN segmentation, and SD-WAN) to support thousands of concurrent users, high-bandwidth multimedia, online learning, and IoT devices while preserving management simplicity through cloud-based tooling.

The architecture designs a hotel-style, multi-tier network architecture for a high-density college apartment to address poor Wi-Fi coverage, insecure device mixing, and scalability challenges common in multi-tenant environments. 

The network segments resident, guest, staff, and IoT traffic using VLANs, enterprise Cisco Meraki hardware, and cloud-managed SD-WAN for resilient connectivity and simplified operations. Deliverables included multi-floor logical and physical network diagrams, IP addressing and DHCP/NAT patterns, a costed hardware and licensing BOM, and security segmentation. 

## Network Architecture & Technical Features

Key Architecture Decisions:

- Layered Design: Core → Distribution → Access for redundancy, predictable routing, and failover.
- VLAN Segmentation: Separate networks for Residents, Guests, Staff, IoT, Management, and Services, with ACLs enforcing isolation and security.
- High-Density Wi-Fi: Optimized MR53 and MR30H placements, channel planning (1/6/11), MIMO, and capacity planning for multimedia, online learning, and gaming.
- SD-WAN Resilience: MX appliances with active/active internet links and centralized policy enforcement for uptime and load balancing.
- Operational Management: Cisco Meraki cloud console for zero-touch provisioning, telemetry monitoring, and automated alerting.
- Cost & Resource Planning: Comprehensive BOM including hardware, SFPs, cabling, mounting, and Meraki licensing tiers.

### Tech Stack & Hardware

Network Hardware:

- Cisco Meraki: MR Access Points, MX Security/SD-WAN Appliances, MS/Catalyst Switches
- Routers/Firewalls: MX250 (SD-WAN & security)
- Core/Distribution Switches: C9300 / C9500 (Ethernet fabric & routing)
- Access Points: MR53, MR30H (high density, hospitality-grade)

Design Patterns & Best Practices:

- Layer-2/Layer-3 segmentation, VLAN isolation, and ACL enforcement
- DHCP scope planning, NAT configuration per VLAN
- Wi-Fi channel planning, band steering, and QoS for multimedia applications
- Monitoring & Observability: Meraki dashboards, SNMP, and integration with third-party tools

## Project Structure

```text
├── diagrams/ 
│   ├── diagram-1.png # Third to eight floor diagram
│   ├── diagram-2.png # Second floor diagram
│   └── diagram-3.png # First floor diagram
├── docs/ 
│   ├── Network_Design.pdf # Full report covering estimated costs, recommendations, and reasoning.
│   └── Floor_Plan.vsdx    # File of the diagram in visio 
└── README.md # Project summary
```

## Diagrams & Documents

Diagrams provide the main artifacts for reviewers. See the 'Network  Design' PDF for further details.

### First Floor - Common Areas & Lobby

![First Floor Diagram](/diagrams/diagram-3.png)  

### Second Floor – Conference & Office Area Layout  

![2 Floor Diagram](/diagrams/diagram-4.png)

### Floors 3 to 8 Floor - Apartment Layout 

![3 to 8 Floor Diagram](/diagrams/diagram-2.png)  

### Floors 3 to 8 Floor - Apartment West Wing Layout 

![3 to 8 West Wing Diagram](/diagrams/diagram-1.png)  
