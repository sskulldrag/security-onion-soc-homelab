# SOC Homelab Architecture

## 1. Architecture Overview

This document describes the physical and logical infrastructure supporting a self-hosted Security Operations Center (SOC) built around Security Onion 3.1.

The environment integrates enterprise-style network segmentation, dedicated security monitoring hardware, Windows Active Directory, Linux endpoints, and centralized security telemetry collection.

The architecture is designed to support:

- Network traffic monitoring and analysis
- Centralized endpoint telemetry collection
- Network segmentation and access control
- Multi-tenant security monitoring
- Security detection and incident investigation
- Controlled security testing and validation

## 2. Physical Infrastructure

### Network Equipment

| Component | Model | Function |
|---|---|---|
| ISP | Cox Communications | Internet connectivity |
| Cable Modem | Netgear Nighthawk CM3000 | DOCSIS 3.1 modem with 2.5GbE |
| Router | TP-Link Omada ER7412-M2 | Gateway, routing, and network access controls |
| Managed Switch | TP-Link Omada SG2210XMP-M2 | 2.5GbE switching, VLANs, PoE+, and port mirroring |
| Wireless Access Point | TP-Link Omada EAP772 | Wi-Fi 7 wireless connectivity |
| Network Controller | TP-Link Omada OC220 | Centralized network management |
| UPS | CyberPower CP1500PFCRM2U | Battery backup and power protection |
| Rack | Tripp Lite SRW12US | Wall-mounted network enclosure |

### Security Onion Server

The Security Onion deployment runs on dedicated physical hardware rather than a virtual machine.

| Component | Specification |
|---|---|
| Motherboard | ASUS ROG Strix B550-F Gaming |
| Processor | AMD Ryzen 5 5600X |
| Memory | 64 GB DDR4 |
| Primary Storage | WD Blue SN750 1 TB NVMe |
| Secondary Storage | Samsung 990 Pro 4 TB NVMe |
| Management Interface | Onboard 1GbE |
| Monitoring Interfaces | Intel X520-DA2 Dual-Port 10GbE SFP+ |
| Operating System | Security Onion 3.1 |
| Deployment Type | Standalone |

The dedicated server provides centralized security monitoring, event collection, indexing, and analysis.

## 3. Network Monitoring Architecture

The managed switch is configured to mirror selected network traffic to a dedicated Security Onion monitoring interface.

This allows Security Onion to observe network communications without requiring endpoints to route their normal traffic through the monitoring server.

The monitoring architecture includes:

- A dedicated management interface for Security Onion administration
- A separate 10GbE monitoring interface
- Switch based traffic mirroring
- Centralized log ingestion through Elastic Agent
- Security analysis through the Security Onion interface and integrated tools

The architecture supports both network based and host based security monitoring.

## 4. Logical Network Architecture

The network uses VLAN segmentation to separate management systems, trusted devices, endpoints, SOC infrastructure, and guest access.

Detailed VLAN assignments, subnet configurations, routing policies, and access control rules will be documented in a separate section.

## 5. Architecture Development Status

The physical infrastructure and core Security Onion deployment are operational.

Additional documentation will cover:

- Network topology diagrams
- VLAN and subnet assignments
- Switch port configuration
- Firewall and access control policies
- Elastic Agent communication paths
- Multi-tenant SOC architecture
- Security validation and testing

This document will be updated as the environment evolves.
