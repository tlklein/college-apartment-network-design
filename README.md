# College Apartment Network Design Project

## Project Overview

This project covers a scalable, secure, and resilient network for a multi-unit college apartment complex. It applies enterprise network principles (layered routing, VLAN segmentation, and SD-WAN) to support thousands of concurrent users, high-bandwidth multimedia, online learning, and IoT devices while preserving management simplicity through cloud-based tooling.

The architecture designs a hotel-style, multi-tier network architecture for a high-density college apartment to address poor Wi-Fi coverage, insecure device mixing, and scalability challenges common in multi-tenant environments. 

The network segments resident, guest, staff, and IoT traffic using VLANs, enterprise Cisco Meraki hardware, and cloud-managed SD-WAN for resilient connectivity and simplified operations. Deliverables included multi-floor logical and physical network diagrams, IP addressing and DHCP/NAT patterns, a costed hardware and licensing BOM, and security segmentation. 

## Project Scope & Features

- Layered Architecture: Core → Distribution → Access for redundancy and predictable routing.  
- VLAN Segmentation: Resident, Guest, Staff, IoT, Management, and Services VLANs with ACLs.  
- High-Density Wi-Fi: MR53 + MR30H placements and channel plan, MIMO considerations, and capacity planning.  
- SD-WAN Resilience: MX appliances for active/active internet links and centralized policy enforcement.  
- Operational Management: Cisco Meraki cloud console for zero-touch provisioning, telemetry, and alerting.  
- Cost Analysis: BOM including devices, SFPs, cabling, mounting, and Meraki licensing tiers.

### Tech & Hardware

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

## Project Structure

```text
├── diagrams/ 
│   ├── diagram-1.png # third to eight floor diagram
│   ├── diagram-2.png # second floor diagram
│   └── diagram-3.png # first floor diagram
├── docs/ 
│   ├── Network_Design.pdf # full report covering estimated costs, recommendations, and reasoning.
│   └── Floor_Plan.vsdx # file of the diagram in visio 
└── README.md
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