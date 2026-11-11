# security-onion-soc-homelab
A hands on cybersecurity homelab featuring Security Onion 3.1, network segmentation, centralized security monitoring, endpoint telemetry, Active Directory, and multi-tenant SOC architecture.
# Security Onion SOC Homelab

## Project Overview

This repository documents the design, deployment, configuration, and ongoing development of a self hosted Security Operations Center (SOC) homelab.

The environment is built around **Security Onion 3.1**, an open-source security monitoring platform, and integrates enterprise networking, Windows Active Directory, Linux endpoints, centralized log collection, and security monitoring technologies.

The purpose of this project is to develop practical experience in security operations, network defense, endpoint monitoring, detection engineering, and security architecture.

The lab also supports a graduate level cybersecurity capstone project focused on evaluating tenant isolation within a shared SOC infrastructure.

## Project Objectives

- Design and implement a segmented network using VLANs and managed networking equipment.
- Deploy and administer a dedicated Security Onion server.
- Integrate Windows and Linux endpoints using Elastic Agent.
- Configure Windows advanced auditing and Sysmon for enhanced endpoint visibility.
- Centralize and analyze security telemetry.
- Implement and evaluate role-based access controls (RBAC) and multi-tenant data isolation.
- Conduct controlled security testing to evaluate monitoring capabilities and access restrictions.
- Document architecture decisions, deployment procedures, troubleshooting, and experimental findings.

## Core Technologies

| Category | Technologies |
|---|---|
| Security Monitoring | Security Onion 3.1, Elasticsearch, Kibana |
| Networking | TP-Link Omada, VLANs, ACLs, Port Mirroring |
| Windows Infrastructure | Windows Server 2022, Active Directory, Group Policy |
| Endpoint Monitoring | Elastic Agent, Sysmon, Windows Event Logs |
| Linux Infrastructure | Ubuntu Server, Linux Mint, Nginx |
| Virtualization | VMware Workstation Pro |
| Security Architecture | RBAC, Multi-Tenancy, Network Segmentation |
| Detection Engineering | MITRE ATT&CK, Atomic Red Team (Planned) |

## Project Documentation

This repository will progressively include:

1. Physical and logical network architecture
2. Hardware inventory and infrastructure specifications
3. VLAN configuration and network segmentation
4. Security Onion installation and configuration
5. Active Directory and endpoint deployment
6. Centralized telemetry collection and monitoring
7. Multi-tenant SOC implementation and isolation testing
8. Detection engineering and security validation
9. Troubleshooting and lessons learned

## Project Status

**Status:** Active Development

This repository is a living technical portfolio. Documentation and experimental results will be added as implementation and validation activities progress.
